---
title: "BadDet: Blockchain Fraud Detection with Dynamic Address-Transaction Graph Convolutional Networks."
authors:
- Xiaoda Wang
- admin
- Tengda Guo
- Zhiyuan Cheng
- Carl Yang 
- Mingjie Tang

- Robert Ford
author_notes:
- "Equal contribution"
- "Equal contribution"
date: "2024-05-16T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-05-16T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "*preprint*"
publication_short: ""

abstract: Bitcoin, a decentralized cryptocurrency, operates on a peer-to-peer Blockchain network that eliminates the need for parties to disclose personal information. This anonymity, however, increases the potential for malicious transactions. While efforts have been made to identify fraudulent Bitcoin transactions, current methods largely overlook behavioral analysis in address classification and the identification of user entity as addresses with similar behaviors. In addition, the dynamic and imbalanced attributes of Bitcoin addresses complicate the detection of anomalous information, which are rarely considered in prior works. In this paper, we propose BadDet, a dynamic Graph Convolutional Network (GCN) framework for fraud detection in Blockchain. Technically, we introduce three key designs. Firstly, we construct the first dynamic Bitcoin address-transaction dataset by transforming Bitcoin addresses and transactions into a heterogeneous graph structure. This dataset includes five types of address behaviors and over 850k real-world
Bitcoin addresses. Secondly, we propose a clustering algorithm to efficiently construct the user entity graph and formulate the user entity features. Lastly, we propose a dynamic GCN which employs an unsupervised feature generation method to derive low-dimensional representations for effective fraudulent address identification. And we adapt GCN along the temporal dimension to dynamically update the weight matrices of different GCN layers. Experimental results show that our proposed framework outperforms state-of-the-art Bitcoin address classifiers, achieving an F1-score of 84.9% and an AUC of 95.8%. We open-source the dataset and our implementations to encourage further research.

# Summary. An optional shortened abstract.
summary: 

tags: ["Blockchain", "Graph Convolutional Network", "Heterogeneous Graph"]
featured: True

# links:
# - name: ""
#   url: ""
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
  caption: 'Overview of BadDet'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

<!-- {{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->
