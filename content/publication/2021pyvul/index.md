---
title: "Intelligent mining vulnerabilities in python code snippets"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Cheng Huang
- Weina Niu
- Yong Fang

# Author notes (optional)
author_notes:
- ""
- "tutor"
- ""
- "tutor"

date: "2021-09-15T00:00:00Z"
doi: '10.3233/JIFS-211011'

# Schedule page publish date (NOT publication's date).
publishDate: "2021-09-15T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: In *Journal of Intelligent & Fuzzy Systems*
publication_short: In *JIFS*

abstract:  In the software development process, many developers learn from code snippets in the open-source community to implement specific functions. However, few people think about whether these code have vulnerabilities, which provides channels for developing unsafe programs. To this end, this paper constructs a source code snippets vulnerability mining system named PyVul based on deep learning to automatically detect the security of code snippets in the open source community. PyVul builds abstract syntax tree (AST) for the source code to extract its code feature, and then introduces the bidirectional long-term short-term memory (BiLSTM) neural network algorithm to detect vulnerability codes. If it is vulnerable code, the further constructed a multi-classification model could analyze the context discussion contents in associated threads, to classify the code vulnerability type based the content description. Compared with traditional detection methods, this method can identify vulnerable code and classify vulnerability type. The accuracy of the proposed model can reach 85%. PyVul also found 138 vulnerable code snippets in the real public open-source community. In the future, it can be used in the open-source community for vulnerable code auditing to assist users in safe development.

# Summary. An optional shortened abstract.
summary: The paper constructs a source code snippets vulnerability mining system named PyVul based on deep learning to automatically detect the security of code snippets in the open source community. 

tags: [Open-source community, vulnerability mining, content analysis, BiLSTM]

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
# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
#   focal_point: ""
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- 2021pyvul


# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: 2021pyvul
---
