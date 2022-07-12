---
title: A Hybrid Semantic Vulnerability Mining System Based on Graph Neural Network
subtitle: 

# Summary for listings and search engines
summary: Traditional vulnerability mining methods have been unable to meet the security analysis needs of complex software because of the high false-positive rate and high false-negative rate. To resolve the existing problems, we propose a graph neural network vulnerability mining system based on hybrid semantics, which constructs a composite semantic code property graph for code representation based on the causes of vulnerabilities. A gated graph neural network is used to extract deep semantic information. Since most of the vulnerabilities are data flow associated, we use taint analysis to extract the taint propagation chain, use the BiLSTM model to extract the token-level features of the context, and finally use the classifier to classify the fusion features. We introduce a dual-attention mechanism that allows the model to focus on vulnerability-related code, making it more suitable for vulnerability mining tasks.

# Link this post with a project
projects: []

# Date published
date: "2021-12-09T00:00:00Z"

# Date updated
lastmod: "2022-05-06T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
#   focal_point: ""
#   placement: 2
#   preview_only: false

authors:
- Computers & Security(Accepted)

tags:
- Code Representation
- Vulnerability Analysis
- Graph Neural Network

categories:
---

## Overview


**Abstract**: In recent years, software programs tend to be large and complex, the software has become the infrastructure of modern society, but software security issues can not be ignored. software vulnerabilities have become one of the main threats to computer security. There are countless cases of exploiting source code vulnerabilities to launch attacks. At the same time, the development of open source software has made source code vulnerability detection more and more critical. Traditional vulnerability mining methods have been unable to meet the security analysis needs of complex software because of the high false-positive rate and high false-negative rate. To resolve the existing problems, we propose a graph neural network vulnerability mining system based on hybrid semantics, which constructs a composite semantic code property graph for code representation based on the causes of vulnerabilities. A gated graph neural network is used to extract deep semantic information. Since most of the vulnerabilities are data flow associated, we use taint analysis to extract the taint propagation chain, use the BiLSTM model to extract the token-level features of the context, and finally use the classifier to classify the fusion features. We introduce a dual-attention mechanism that allows the model to focus on vulnerability-related code, making it more suitable for vulnerability mining tasks. The experimental results show that HyVulDect outperforms existing state-of-the-art methods and can achieve an accuracy rate of 92\% on the benchmark dataset. Compared with the rule-based static mining tools Flawfinder, RATS, and Cppcheck, it has better performance and can effectively detect the actual CVE source code vulnerabilities.