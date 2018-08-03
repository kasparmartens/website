+++
title = "Neural Processes as distributions over functions"

date = 2018-08-02T00:00:00
lastmod = 2018-08-02T00:00:00
draft = false
math = true

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = []

tags = []
summary = "What are Neural Processes and how they behave as a distribution over functions?"

[header]
image = ""
caption = ""


+++

In this year’s ICML, some interesting work was presented on Neural Processes. See the paper [conditional Neural Processes](https://arxiv.org/abs/1807.01613) and the follow-up work by the same authors on [Neural Processes](https://arxiv.org/abs/1807.01622) which was presented in the workshop. 

Neural Processes (NPs) caught my attention as they essentially are a neural network (NN) based probabilistic model which can represent a distribution over stochastic processes. So NPs combine elements from two worlds: 

* Deep Learning -- a neural network is a flexible non-linear function which is straightforward to train
* Gaussian Processes -- GPs offer a probabilistic framework for learning a distribution over a wide class of non-linear functions

Both have their advantages and drawbacks. In the limited data regime, GPs are preferable due to their probabilistic nature and ability to capture uncertainty. This differs from (non-Bayesian) NNs which represent a single function rather than a distribution over functions. However the latter might be preferable in the presence of large amounts of data as training NNs is computationally much more scalable than inference for GPs. Neural Processes aim to combine the best of these two worlds. 

I found the idea behind NPs interesting, but I felt I was lacking intuition and a deeper understanding how NPs behave as a prior over functions. I believe, often the best way towards understanding something is implementing it, empirically trying it out on simple problems, and finally explaining this to someone else. So here is my attempt at reviewing and discussing NPs. 

### What is a Neural Process?

The NP is a neural network based approach to represent a distribution over functions. The broad idea behind how the NP model is set up and how it is trained is illustrated in this schema:

![](https://raw.githubusercontent.com/kasparmartens/NeuralProcesses/master/fig/schema1.png)

Given a set of observations $(x_i, y_i)$, they are split into two sets: "context points" and "target points". Given the pairs $(x_c, y_c)$ for $c = 1, …, C$ in the context set and given unseen inputs $x_t^{\ast}$ for $t = 1, …, T$ in the target set, our goal is to predict the corresponding function values $y_t^{\ast}$. We can think of NPs as if they were modelling the target set conditional on the context. Information flows from the context set (on the left) to making new predictions on the target set (on the right) via the latent space $z$. The latter is essentially a finite-dimensional embedding of mappings from x to y. The fact that $z$ is a random variable makes NP a probabilistic model and lets us capture uncertainty over functions. Once we have trained the model, we can use the (approximate) posterior distribution of $z$ to make predictions at test time. 

At first sight, the split into context and target sets may look like the standard train and test split of the data, but this is not the case, as the target set is directly used in training the NP model -- our (probabilistic) loss function is explicitly defined over the target set. This will allow the model to avoid overfitting and achieve better out-of-sample generalisation. In practice, we would repeatedly split out training data into randomly chosen context and target sets to obtain good generalisation. 

Let us consider two scenarios: 

1. Inferring a distribution over functions, based on a single data set
2. Inferring a distribution over functions, when we have access to multiple data sets which we believe to be related in some way

The first scenario corresponds to a standard (probabilistic) supervised learning setup: Given a data set of $N$ samples, i.e. given $(x_i, y_i)$ for $i = 1, … ,N$, and assuming there is an underlying true $f$ which has generated the $y_i = f(x_i)$ values, our goal is to learn the posterior distribution over $f$ and use it to get predictive densities at test points $f(x^{\ast})$.

[insert-figure]

The second scenario can be seen from the meta-learning viewpoint. Given $D$ data sets $d = 1, …, D$, each consisting of $N_d$ pairs $(x_i^{(d)}, y_i^{(d)})$, if we assume that every data set $d = 1, …, D$ has its own underlying function $f_d$ which has generated the values $y_i = f_d(x_i)$, we might want to learn the posterior of every $f_d$ as well as generalise to a new data set $d^{\ast}$. The latter is especially useful when every data set has only a small number of observations. This information sharing is achieved by specifying that there exists a shared process which underlies all functions $f_d$. For example, in the context of GPs, one can assume that $f_d \sim \mathcal{GP}$ share kernel hyperparameters. Having learned the shared process, when given a new data set $d^{\ast}$, one can use the posterior over functions as a prior and carry out few-shot function regression. 

The reason I wanted to highlight these two scenarios is the following: Usually, in the most standard setting, GP-regression is carried out under the first scenario. This tends to work well even when $N$ is small. However, the motivation behind NPs seems to be mainly coming from the meta-learning setup -- in this setting the latent $z$ can be thought of as a mechanism to share information across different data sets. Nevertheless, having elements of a probabilistic model, NPs should be applicable in both scenarios. Below we will investigate how NPs behave when trained only on a single data set, as well as the second setup where we have access to a large number of function draws in order to train the NP. 

### How are NPs implemented?

Here is a more detailed schema of the NP generative model: 

![](https://raw.githubusercontent.com/kasparmartens/NeuralProcesses/master/fig/schema2.png)


Going through this generative mechanism step-by-step:

* First, the context points $(x_c, y_c)$ are mapped through a NN $h$ to obtain a latent representation $r_c$. 
* Then, the vectors $r_c$ are aggregated (in practice: averaged) to obtain a single value $r$ (which has the same dimensionality as every $r_c$). 
* This $r$ is used to parametrise the distribution of $z$, i.e. $p(z | x\_{1:C}, y\_{1:C}) = \mathcal{N}(\mu_z( r ), \sigma_z^2( r ))$
* Finally, to obtain a prediction at a target $x_t^{\ast}$, we sample $z$ and concatenate this with $x_t^{\ast}$, and map $(z, x_t^{\ast})$ through a NN $g$ to obtain a sample from the predictive distribution of $y_t^{\ast}$. 


Inference for the NP is carried out in the variational inference framework. Specifically, we introduce two approximate distributions: 

* $q(z | context)$ to approximate the conditional prior $p(z | context)$
* $q(z | context, target)$ to approximate the respective $p(z | context, target)$
where we have denoted $\text {context} := (x\_{1:C}, y\_{1:C})$ and $\text {target} := (x\_{1:T}, y\_{1:T})$. 

The approximate posterior $q(z | \cdot)$ is chosen to have the specific form as illustrated in the inference model diagram below. That is, we use the same $h$ to map both the context set as well as the target set to obtain the aggregated $r$, which in turn is mapped to $\mu_z$ and $\sigma_z$. These parametrise the approximate posterior $q(z | \cdot) = \mathcal{N}(\mu_z, \sigma_z)$. 

![](https://raw.githubusercontent.com/kasparmartens/NeuralProcesses/master/fig/schema3.png)

The variational lower bound 

$$ELBO = …$$

contains two terms. The first is the expected log-likelihood over the target set. This is evaluated by sampling $z \sim q(z | context, target)$, as indicated on the left part of the inference diagram, and then using these $z$ values for predictions on the target set. The second term has a regularising effect -- it is the KL divergence between $q(z | context, target)$ and $q(z | context)$. Note that this differs slightly from the most commonly encountered variational inference setup with $\text{KL}(q || p)$, where $p$ would be the prior of $z$. This is because in our generative model, we have specified a conditional prior $p(z | context)$ instead of directly specifying $p(z)$. And as this conditional prior depends on $h$, we need to use an approximate $q(z | context)$.

### Experiments
