---
title: 'Interleaved Scene Graph for Interleaved Text-and-Image Generation Assessment'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Dongping Chen
  - Ruoxi Chen
  - Shu Pu
  - admin
  - Yanru Wu
  - Caixi Chen
  - Benlin Liu
  - Yue Huang
  - Yao Wan
  - Pan Zhou
  - Ranjay Krishna

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'
  - ''
  - ''
  - ''
  - ''
  - 'Corresponding author'

date: '2024-09-02T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2024-09-01T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *Thirteenth International Conference on Learning Representations (ICLR 2025, In Submission)*
publication_short: In *Thirteenth International Conference on Learning Representations (ICLR 2025, In Submission)*

abstract: Unified Transformer-based models have enabled simultaneous multimodal understanding and generation, showing promise in unifying both vision and language tasks with interleaved text-and-image generation. However, assessing the performance of multimodal interleaved generation remains unexplored and challenging due to the complexity of interleaved content. We design an automatic multi-granular evaluation framework called Interleaved Scene Graph (ISG). ISG evaluates generations across four levels of granularity; for each granular evaluation, ISG converts each query into a set of atomic questions, which probes for various aspects of correctness. Using ISG, we introduce ISG-Bench, the first multimodal interleaved benchmark with concrete generation requirements for 1,150 queries, spanning a diverse set of 21 text-image generation tasks.

In our experiments, we conduct a multi-granular evaluation of ISG, demonstrating its potential for automatically evaluating interleaved generation consistent with ground truth and human preferences. Furthermore, comprehensive assessments of 10 interleaved generative frameworks reveal that unified models still lack basic accurate instruction-following capabilities, falling short even in structural requirements. Additionally, we introduce a baseline in a compositional agent framework ISG-Agent to explore the upper bound of interleaved generation with agent workflow, outperforming other compositional frameworks in interleaved generation at various levels but still struggles with vision-dominated tasks. Our work offers valuable insights for advancing future research in interleaved generation.

# Summary. An optional shortened abstract.
# summary: 

tags: ["Interleaved Text-and-Image Generation"]

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://openreview.net/pdf?id=rDLgnYLM5b'
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
  caption: 'High Light Overview of ISG'
  focal_point: ''
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
Click the _Cite_ button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the _Slides_ button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->
