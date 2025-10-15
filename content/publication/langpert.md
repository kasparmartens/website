+++
title = "LangPert: LLM-Driven Contextual Synthesis for Unseen Perturbation Prediction"
date = "2025-04-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["K Märtens", "M Boubnovski Martell", "C Prada", "R Donovan-Maiye"]

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
publication = "MLGenX at ICLR 2025 (selected as Oral Presentation)"
publication_short = "MLGenX at ICLR 2025 (selected as Oral Presentation)"

# Abstract and optional shortened version.
abstract = "Systematic genetic perturbation provides critical insights into cell functioning, yet predicting their cellular effects remains a major challenge. Despite advances in computational approaches, accurately modelling cellular responses to unseen perturbations continues to be difficult. Large Language Models (LLMs) have shown promise in biological applications by synthesizing scientific knowledge, but their direct application to high-dimensional gene expression data has been impractical due to numerical limitations. We propose LangPert, a novel hybrid framework that leverages LLMs to guide a downstream k-nearest neighbors (kNN) aggregator, combining biological reasoning with efficient numerical inference. We demonstrate that LangPert achieves state-of-the-art performance on single-gene perturbation prediction tasks across multiple datasets."

abstract_short = "LangPert combines Large Language Models with numerical methods (kNN) to predict cellular responses to genetic perturbations, overcoming LLMs' limitations with high-dimensional genomic data while achieving state-of-the-art performance."

# Featured image thumbnail (optional)
image_preview = "langpert_banner.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = []

# Links (optional).
url_pdf = "https://openreview.net/forum?id=Tmx4o3Jg55"
url_code = ""
# url_dataset = "#"
# url_project = "#"
url_slides = ""
url_video = ""
url_poster = ""
url_github = ""
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
image = "langpert_banner.png"
caption = ""

+++
