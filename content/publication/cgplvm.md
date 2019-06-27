+++
title = "Decomposing feature-level variation with Covariate Gaussian Process Latent Variable Models"
date = "2019-06-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["K Märtens", "K Campbell", "C Yau"]

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
publication = "Accepted to *ICML* (2019)"
publication_short = "Accepted to *ICML* (2019)"

# Abstract and optional shortened version.
abstract = "The interpretation of complex high-dimensional data typically requires the use of dimensionality reduction techniques to extract explanatory low-dimensional representations. However, in many real-world problems these representations may not be sufficient to aid interpretation on their own, and it would be desirable to interpret the model in terms of the original features themselves. Our goal is to characterise how feature-level variation depends on latent low-dimensional representations, external covariates, and non-linear interactions between the two. In this paper, we propose to achieve this through a structured kernel decomposition in a hybrid Gaussian Process model which we call the Covariate Gaussian Process Latent Variable Model (c-GPLVM). We demonstrate the utility of our model on simulated examples and applications in disease progression modelling from high-dimensional gene expression data in the presence of additional phenotypes. In each setting we show how the c-GPLVM can extract low-dimensional structures from high-dimensional data sets whilst allowing a breakdown of feature-level variability that is not present in other commonly used dimensionality reduction approaches."

abstract_short = "The interpretation of high-dimensional data typically requires the use of dimensionality reduction techniques. However, in many real-world problems the extracted low-dimensional representations may not be sufficient to aid interpretation on their own, and it would be desirable to interpret the model in terms of the original features themselves. Our goal is to characterise how *feature-level* variation depends on latent low-dimensional representations, external covariates, and non-linear interactions between the two. Here, we propose to achieve this through a structured kernel decomposition in a hybrid Gaussian Process model which we call the Covariate Gaussian Process Latent Variable Model (c-GPLVM)."

# Featured image thumbnail (optional)
image_preview = "cGPLVM_cover.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = []

# Links (optional).
url_pdf = "http://proceedings.mlr.press/v97/martens19a.html"
# url_preprint = "https://arxiv.org/abs/1810.06983"
url_code = "https://github.com/kasparmartens/c-GPLVM"
# url_dataset = "#"
# url_project = "#"
url_slides = "https://icml.cc/media/Slides/icml/2019/201(11-16-00)-11-16-20-4994-decomposing_fea.pdf"
url_video = "https://slideslive.com/38916814/general-ml"
url_poster = "https://pbs.twimg.com/media/D8YnUOBXYAAvKnX?format=jpg"
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
image = "cGPLVM_cover.png"
caption = ""

+++

