+++
title = "Covariate Gaussian Process Latent Variable Models"
date = "2018-12-01"

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
publication_types = ["0"]

# Publication name and optional abbreviated version.
publication = "Preprint (2018)"
publication_short = "Preprint (2018)"

# Abstract and optional shortened version.
abstract = "Gaussian Process Regression (GPR) and Gaussian Process Latent Variable Models (GPLVM) offer a principled way of performing probabilistic non-linear regression and dimensionality reduction. In this paper we propose a hybrid between the two, the covariate-GPLVM (c-GPLVM), to perform dimensionality reduction in the presence of covariate information (e.g. continuous covariates, class labels, or censored survival times). This construction lets us adjust for covariate effects and reveals meaningful latent structure which is not revealed when using GPLVM. Furthermore, we introduce structured decomposable kernels which will let us interpret how the fixed and latent inputs contribute to feature-level variation, e.g. identify the presence of a non-linear interaction. We demonstrate the utility of this model on applications in disease progression modelling from high-dimensional gene expression data in the presence of additional phenotypes."

abstract_short = "Dimensionality reduction is a key step towards gaining insights into complex high-dimensional data. However, real-life data often exhibits strong structure which is *a priori* known to us. This could be in various forms of covariate information (e.g. continuous measurements, class labels, or censored survival times). Here, we propose the covariate-GPLVM to learn a covariate-adjusted low-dimensional representation which would reveal meaningful latent structure shared across different class labels or covariate values."

# Featured image thumbnail (optional)
image_preview = "cGPLVM_cover.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = []

# Links (optional).
# url_pdf = ""
url_preprint = "https://arxiv.org/abs/1810.06983"
# url_code = ""
# url_dataset = "#"
# url_project = "#"
# url_slides = "#"
# url_video = "#"
# url_poster = ""
# url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Link to paper", url = "https://doi.org/10.1093/bioinformatics/btw304"}]

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

The preprint is available on [arxiv](https://arxiv.org/abs/1810.06983).