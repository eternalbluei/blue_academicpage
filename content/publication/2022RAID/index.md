---
title: "Viopolicy-Detector: An Automated Approach to Detecting GDPR Compliance Violations in Websites"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- Haoran Ou
- Yong Fang
- admin
- Yongyan Guo

# Author notes (optional)
author_notes:
- ""
- "tutor"

date: "2022-06-12T00:00:00Z"
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: "2022-06-12T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *The 25th International Symposium on Research in Attacks, Intrusions and Defenses*
publication_short: In *RAID(2022)*

abstract: To provide users with personalized services, the website collects and tracks user’s activity data. At the same time, each website uses a privacy policy to ensure the legality of these actions. The purpose of the implementation of the General Data Protection Regulation (GDPR) is to protect the privacy of user data. Because GDPR is a programmatic regulation, there is no specific guidance on what a privacy policy should contain. Therefore, there may still be potential violations on the website, thus cause a risk of leak users’ private data. In this paper, we define a violating behavior that data collected by the website without a declaration in the privacy policy is illegal. To complete the violating behavior detection, we first interpret the GDPR and analyze 1000 website privacy policies to present a personal data classification including eight categories. Based on this, we propose a privacy policy annotation scheme including these eight categories and collect 145 related Web APIs. Then we propose an automated method to detect GDPR compliance violations in websites. On the one hand we use the multi-label text classification model to extract data collection stated in the privacy policy, with a precision of 0.9817. For another, We dynamically monitor the JavaScript calls of the website related to personal data collection during user visits. Finally, we compare the two results to determine whether violating behaviors appeared. We use this method to detect the European top 500 websites. A total of 159 websites appear in violation of the GDPR. We analyze the detection results from different perspectives, including statistics on the types of data declared in the privacy policy, statistics on data collected by the website, and which data collection is likely to cause violations. Then we classify the violating websites and find that websites in the Social category present the most violations. Finally, we count the rankings of the offending websites. Surprisingly, top-ranking sites are even more prone to breaches. There are even some globally well-known websites with violations, such as BBC, Nokia, Ebay, Google etc.

# Summary. An optional shortened abstract.
summary: We propose a privacy policy annotation scheme including these eight categories and collect 145 related Web APIs. Then we propose an automated method to detect GDPR compliance violations in websites.

tags: [privacy policy, GDPR violation, Web API, inconsistent data collection]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
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
- 2022RAID

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: 2022RAID
---

