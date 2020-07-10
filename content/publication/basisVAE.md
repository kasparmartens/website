+++
title = "BasisVAE: Translation-invariant feature-level clustering with Variational Autoencoders"
date = "2020-03-08"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["K Märtens", "C Yau"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["0"]

# Publication name and optional abbreviated version.
publication = "Accepted to *AISTATS* (2020)"
publication_short = "Accepted to *AISTATS* (2020)"

# Abstract and optional shortened version.
abstract = "Variational Autoencoders (VAEs) provide a flexible and scalable framework for non-linear dimensionality reduction. However, in application domains such as genomics where data sets are typically tabular and high-dimensional, a black-box approach to dimensionality reduction does not provide sufficient insights. Common data analysis workflows additionally use clustering techniques to identify groups of similar features. This usually leads to a two-stage process, however, it would be desirable to construct a joint modelling framework for simultaneous dimensionality reduction and clustering of features. In this paper, we propose to achieve this through the BasisVAE: a combination of the VAE and a probabilistic clustering prior, which lets us learn a one-hot basis function representation as part of the decoder network. Furthermore, for scenarios where not all features are aligned, we develop an extension to handle translation-invariant basis functions. We show how a collapsed variational inference scheme leads to scalable and efficient inference for BasisVAE, demonstrated on various toy examples as well as on single-cell gene expression data."

abstract_short = "It would be desirable to construct a joint modelling framework for simultaneous dimensionality reduction and clustering of features. Here, we focus on embedding such capabilities within the Variational Autoencoder (VAE) framework. Specifically, we propose the BasisVAE: a combination of the VAE and a probabilistic clustering prior, which lets us learn a one-hot basis function representation as part of the decoder network. Furthermore, for scenarios where not all features are aligned, we develop an extension to handle translation-invariant basis functions."

# Featured image thumbnail (optional)
image_preview = "BasisVAE_schema.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = []

# Links (optional).
url_pdf = "https://arxiv.org/abs/2003.03462"
url_code = "https://github.com/kasparmartens/BasisVAE"
# url_dataset = "#"
# url_project = "#"
url_slides = ""
url_video = ""
url_poster = ""
# url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Link to paper", url = "http://proceedings.mlr.press/v97/martens19a.html"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "BasisVAE_schema.png"
caption = ""

+++

