+++
title = "Augmented Ensemble MCMC sampling in Factorial Hidden Markov Models"
date = "2018-09-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["K Märtens", "MK Titsias", "C Yau"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = "Accepted to *AISTATS* (2019)"
publication_short = "Accepted to *AISTATS* (2019)"

# Abstract and optional shortened version.
abstract = "Bayesian inference for factorial hidden Markov models is challenging due to the exponentially sized latent variable space. Standard Monte Carlo samplers can have difficulties effectively exploring the posterior landscape and are often restricted to exploration around localised regions that depend on initialisation. We introduce a general purpose ensemble Markov Chain Monte Carlo (MCMC) technique to improve on existing poorly mixing samplers. This is achieved by combining parallel tempering and an auxiliary variable scheme to exchange information between the chains in an efficient way. The latter exploits a genetic algorithm within an augmented Gibbs sampler. We compare our technique with various existing samplers in a simulation study as well as in a cancer genomics application, demonstrating the improvements obtained by our augmented ensemble approach."

abstract_short = "Here, we introduce an augmented ensemble MCMC technique to improve on existing poorly mixing samplers for factorial HMMs. This is achieved by combining parallel tempering and an auxiliary variable scheme to exchange information between the chains in an efficient way."

# Featured image thumbnail (optional)
image_preview = "crossover_anim.gif"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = []

# Links (optional).
url_pdf = "http://proceedings.mlr.press/v89/martens19a.html"
# url_preprint = "https://arxiv.org/abs/1703.08520"
url_code = "https://github.com/kasparmartens/ensembleFHMM"
# url_dataset = "#"
# url_project = "#"
# url_slides = "#"
# url_video = "#"
url_poster = "poster/ensemblemcmc_poster.pdf"
# url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Link to paper", url = "http://proceedings.mlr.press/v89/martens19a.html"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "ensemble_logposteriors.png"
caption = ""

+++

This work has been accepted to AISTATS 2019. The updated version of the paper will be soon made available!
