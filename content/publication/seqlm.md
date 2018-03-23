+++
title = "seqlm: an MDL Based Method for Identifying Differentially Methylated Regions in High Density Methylation Array Data"
date = "2016-05-13"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["R Kolde&ast;", "K Märtens&ast;", "K Lokk", "S Laur", "J Vilo"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["2"]

# Publication name and optional abbreviated version.
publication = "In *Bioinformatics*"
publication_short = "In *Bioinformatics*"

# Abstract and optional shortened version.
abstract = "**Motivation:** One of the main goals of large scale methylation studies is to detect differentially methylated loci. One way is to approach this problem sitewise, i.e. to find differentially methylated positions (DMPs). However, it has been shown that methylation is regulated in longer genomic regions. So it is more desirable to identify differentially methylated regions (DMRs) instead of DMPs. The new high coverage arrays, like Illuminas 450k platform, make it possible at a reasonable cost. Few tools exist for DMR identification from this type of data, but there is no standard approach. <br/> **Results:** We propose a novel method for DMR identification that detects the region boundaries according to the minimum description length (MDL) principle, essentially solving the problem of model selection. The significance of the regions is established using linear mixed models. Using both simulated and large publicly available methylation datasets, we compare seqlm performance to alternative approaches. We demonstrate that it is both more sensitive and specific than competing methods. This is achieved with minimal parameter tuning and, surprisingly, quickest running time of all the tried methods. Finally, we show that the regional differential methylation patterns identified on sparse array data are confirmed by higher resolution sequencing approaches."

abstract_short = "Short abstract HERE"

# Featured image thumbnail (optional)
image_preview = "seqlm_merged.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = []

# Links (optional).
url_pdf = "https://doi.org/10.1093/bioinformatics/btw304"
url_code = "https://github.com/raivokolde/seqlm"
# url_preprint = "#"
# url_dataset = "#"
# url_project = "#"
# url_slides = "#"
# url_video = "#"
# url_poster = "#"
url_source = "#"

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
image = "seqlm_merged.png"
caption = "My caption :smile:"

+++

More detail can easily be written here using *Markdown* and $\rm \LaTeX$ math code.