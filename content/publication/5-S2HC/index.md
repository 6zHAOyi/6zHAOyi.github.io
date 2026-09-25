---
title: 'Spectral-Sphere-Constrained Hyper-Connections'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Haichuan Zhang
  - Ang Li

# Author notes (optional)
author_notes:

date: '2026-09-24T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2026-09-24T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *Conference on Neural Information Processing Systems (NeurIPS 2026)*
publication_short: In *Conference on Neural Information Processing Systems (NeurIPS 2026)*

abstract: Hyper-Connections (HC) extend residual connections into multiple streams, employing residual matrices for cross-stream mixing to enrich model expressivity. However, unconstrained mixing disrupts the identity mapping property intrinsic to the residual connection, causing unstable training. To address this, Manifold-Constrained Hyper-Connections (mHC) and its variants restrict these matrices to be doubly stochastic via Sinkhorn-Knopp (SK) algorithm or permutation-based parameterizations. We reveal three limitations of this doubly stochastic constraint:(1) identity degeneration, where learned matrices collapse around the identity initialization and diminish cross-stream interactions, (2) a expressivity bottleneck, where the doubly stochastic constraint restricts the freedom of the subdominant spectrum of the residual matrices, preventing the model from selectively preserving or attenuating cross-stream variations, and (3) parameterization inefficiencies, manifesting as unstable SK iterations or the factorial-scaling overhead of permutation-based parameterizations. To overcome these flaws, we propose Spectral-Sphere-Constrained Hyper-Connections ($\mathrm{s}^{2}$HC). By confining residual matrices to a spectral norm sphere, $\mathrm{s}^{2}$HC restores free control over the subdominant spectrum, enabling the model to selectively preserve or attenuate cross-stream variations. This shift eliminates unstable SK iterations and factorial parameterization, enabling expressive, non-degenerate residual matrices while preserving training stability.

# Summary. An optional shortened abstract.
# summary: 

tags: ["Hyper-Connections"]

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: 'https://github.com/6zHAOyi/s2HC'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# image:
#   caption: 'High Light Overview of BadVision'
#   focal_point: ''
#   preview_only: false

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
