+++
title = "Augmented Ensemble MCMC sampling in Factorial Hidden Markov Models"
date = "2017-06-01"

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
publication_types = ["0"]

# Publication name and optional abbreviated version.
publication = ""
publication_short = ""

# Abstract and optional shortened version.
abstract = "Bayesian inference for factorial hidden Markov models is challenging due to the exponentially sized latent variable space. Standard Monte Carlo samplers can have difficulties effectively exploring the posterior landscape and are often restricted to exploration around localised regions that depend on initialisation. We introduce a general purpose ensemble Markov Chain Monte Carlo (MCMC) technique to improve on existing poorly mixing samplers. This is achieved by combining parallel tempering and an auxiliary variable scheme to exchange information between the chains in an efficient way. The latter exploits a genetic algorithm within an augmented Gibbs sampler. We compare our technique with various existing samplers in a simulation study as well as in a cancer genomics application, demonstrating the improvements obtained by our augmented ensemble approach."

abstract_short = "We introduce an augmented ensemble MCMC technique to improve on existing poorly mixing samplers. This is achieved by combining parallel tempering and an auxiliary variable scheme to exchange information between the chains in an efficient way."

# Featured image thumbnail (optional)
image_preview = "schema_crossover.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = []

# Links (optional).
# url_pdf = ""
# url_code = ""
# url_preprint = "#"
# url_dataset = "#"
# url_project = "#"
# url_slides = "#"
# url_video = "#"
# url_poster = "#"
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
image = ""
caption = "My caption :smile:"

+++

More detail can easily be written here using *Markdown* and $\rm \LaTeX$ math code.