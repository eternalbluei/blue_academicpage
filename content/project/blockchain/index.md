---
title: Digital Currency Fraud Website Detection System
summary: The project proposes a QR code logistics privacy protection system based on segmented encryption and timing control. The system adopts information encryption and concealment technology to encrypt all information of users in segments and then embed them in QR codes of courier face slips. The system automatically generates viewing keys of corresponding authority and distributes them to logistics consolidation center managers of different levels to complete access control for different roles.

tags:
- Digital Currency
- Context Analysis
- Web Development

date: "2021-02-12T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: 
url_code: "https://github.com/lxyeternal/Express-android"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

publication: 2021block
---

**Role**: The main participants.

**Research Background**: The rapid development of blockchain technology has triggered many incidents of digital currency fraud. One of the most common methods is to lure victims into making investments. Cyber criminals usually design the layout of digital currency fraud websites to resemble regular digital currency websites. Using some words related to blockchain, digital currency and project whitepapers to confuse the victims to invest. And its high anonymity makes it difficult to trace.

**Research purposes**: Effective identification of existing digital fraud sites to prevent users from being scammed.

**Research Method**: Firstly, we use crawlers to collect the content of websites and related information to build the dataset, and for inaccessible websites, we use snapshot websites to collect them. Then the collected data were preprocessed to get the blacklist and whitelist data that meet the requirements. After statistical analysis, we select features such as text keywords, search engines, website rankings (e.g. Alexa ranking), domain names and mainstream transactions to generate feature vectors as inputs for the detection model, and finally construct a random forest model for detection.

**Research Results**: We have implemented a digital currency fraud website detection system, which can effectively detect suspicious digital currency websites. Compared with the existing Tencent detection engine, our system can detect many websites that it cannot detect.

**System Show**: 

![block2.png](https://s2.loli.net/2022/04/24/SWNjgxaihr3Xzle.png)

![block1.png](https://s2.loli.net/2022/04/24/veGkpBwZc4uJOLX.png)

![block3.png](https://s2.loli.net/2022/04/24/cVbo56N9GHQTew7.png)
