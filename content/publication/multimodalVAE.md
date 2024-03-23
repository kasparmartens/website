+++
title = "Disentangling shared and private latent factors in multimodal Variational Autoencoders"
date = "2023-12-01"

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
publication = "Accepted to *MLCB* (2023)"
publication_short = "Accepted to *MLCB* (2023)"

# Abstract and optional shortened version.
abstract = "Generative models for multimodal data permit the identification of latent factors that may be associated with important determinants of observed data heterogeneity. Common or shared factors could be important for explaining variation across modalities whereas other factors may be private and important only for the explanation of a single modality. Multimodal Variational Autoencoders, such as MVAE and MMVAE, are a natural choice for inferring those underlying latent factors and separating shared variation from private. In this work, we investigate their capability to reliably perform this disentanglement. In particular, we highlight a challenging problem setting where modality-specific variation dominates the shared signal. Taking a cross-modal prediction perspective, we demonstrate limitations of existing models, and propose a modification how to make them more robust to modality-specific variation. Our findings are supported by experiments on synthetic as well as various real-world multi-omics data sets."

abstract_short = "Here, we investigate the capabilities of Multimodal Variational Autoencoders, such as MVAE and MMVAE, to reliably infer *private* and *shared* latent factors from multi-omics data. In particular, we highlight a challenging problem setting where modality-specific variation dominates the shared signal. Taking a cross-modal prediction perspective, we discuss and demonstrate limitations of existing models, and propose a modification how to make them more robust to modality-specific variation."

# Featured image thumbnail (optional)
image_preview = "multimodalVAE_fig1.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = []

# Links (optional).
url_pdf = "https://proceedings.mlr.press/v240/martens24a.html"
url_code = "https://github.com/kasparmartens/shared-private-multimodalVAE"
# url_dataset = "#"
# url_project = "#"
url_slides = ""
url_video = "https://www.youtube.com/watch?v=T6-OfbLcGdk"
url_poster = ""
url_github = "https://github.com/kasparmartens/shared-private-multimodalVAE"
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
image = "multimodalVAE_fig1.png"
caption = ""

+++
