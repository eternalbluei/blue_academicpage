---
title: "HyVulDect: A Hybrid Semantic Vulnerability Mining System Based on Graph Neural Network"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Yong Fang
- Haoran Ou
- Cheng Huang
- Chun Lin
- Yongyan Guo

# Author notes (optional)
author_notes:
- ""
- "tutor"
- ""
- "tutor"

date: "2022-06-30T00:00:00Z"
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: "2022-06-30T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: In *Computer & Security*
publication_short: In *C&S*

abstract: Traditional vulnerability mining methods have been unable to meet the security analysis needs of complex software because of the high false-positive rate and high false-negative rate. To resolve the existing problems, we propose a graph neural network vulnerability mining system based on hybrid semantics, which constructs a composite semantic code property graph for code representation based on the causes of vulnerabilities. A gated graph neural network is used to extract deep semantic information. Since most of the vulnerabilities are data flow associated, we use taint analysis to extract the taint propagation chain, use the BiLSTM model to extract the token-level features of the context, and finally use the classifier to classify the fusion features. We introduce a dual-attention mechanism that allows the model to focus on vulnerability-related code, making it more suitable for vulnerability mining tasks.

# Summary. An optional shortened abstract.
summary: We propose a graph neural network vulnerability mining system based on hybrid semantics, which constructs a composite semantic code property graph for code representation based on the causes of vulnerabilities.

tags: [Code Representation, Vulnerability Analysis, Graph Neural Network]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://www.sciencedirect.com/science/article/pii/S0167404822002176'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- 2022HyVulDect

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: 2022HyVulDect
---

