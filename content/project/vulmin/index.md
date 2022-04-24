---
title: Vulnerability mining research for open source communities
summary: This project studies the security of source code fragments in open source communities, extracts the core code associated with vulnerabilities through program slicing techniques, and constructs a BiLSTM model for malicious code detection. The text features of posts are also constructed using TF-IDF to train OVO SVMs models for vulnerability code type identification.
tags:
- Deep Learning
- Open Source
- Graph Neural Network
- Code Representation
- Vulnerability Mining
- Program Slices

date: "2020-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

# links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen
url_code: ""
url_pdf: "https://1drv.ms/b/s!AoqulfGeUkjqhOB3B7yMM1Eo_7Y4hQ?e=f13zz9"
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: 
---

**Role**: Project Leader.

**Participation**: Responsible for all aspects of the project, including data collection, data cleaning, program slicing, model building, system implementation, etc.

**Research Background**: In the software lifecycle, most of the vulnerabilities come from the development phase. In the process of completing software development, developers will largely copy some code through some open source communities including StackOverFlow, GitHub to complete a specific function, but few people will consider whether the code on it is safe, if some attackers maliciously upload some code or programs containing vulnerabilities, and developers do not carefully review the direct reference to their own software If some attackers maliciously upload some code or programs containing vulnerabilities, and the developers do not carefully review them and directly refer to their software, then it is very likely to leave a fatal vulnerability.

**Research purposes**: Research on vulnerability detection of Python code snippets for the open source community to assist users in secure development.


**Research Method**: The source code and text files are extracted separately for the posts in the open source community, and the redundant code is removed using program slicing techniques to extract the core code associated with the vulnerability and build a BiLSTM model for malicious code detection. At the same time, we use TF-IDF to construct text features of posts and train OVO SVMs models for vulnerability code type identification. The results of the combined two modules can achieve the identification and type determination of vulnerabilities.


**Project Features**: 
- A new approach to vulnerability mining by fusing code detection and context analysis
- Program slicing techniques for code snippets

**Research Results**: We have implemented PyVul, a Python code snippets detection system for the open source community, which can achieve 85% accuracy and also successfully detects a lot of vulnerable code existing in the open source community.

