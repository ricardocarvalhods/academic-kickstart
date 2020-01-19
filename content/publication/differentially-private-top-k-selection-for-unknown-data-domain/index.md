---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Differentially Private Top-k Selection for Unknown Data Domain"
authors: ["Ricardo Silva Carvalho", "Ke Wang", "Lovedeep Gondara"]
date: 2020-01-06T18:58:22-03:00
doi: ""
share: true
profile: true
commentable: true
math: true

# Schedule page publish date (NOT publication's date).
publishDate: 2020-01-15T18:58:22-03:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "23rd International Conference on Artificial Intelligence and Statistics (**AISTATS 2020**)"
publication_short: "**AISTATS 2020**"

abstract: "We propose new methods that satisfy approximate differential privacy for top-$k$ selection on the unknown data domain setting, not relying on knowledge of domain universe and without assuming any structure of the data. Different from classical methods, our algorithms only require looking at the top-$\\bar{k}$ elements for any $\\bar{k} \\geq k$. By not requiring knowledge of domain and limiting the elements considered, we enforce the principle of minimal privilege, which requires granting the strictly necessary access for a given task. Additionally, we also design a novel way of optimizing the choice of $\\bar{k}$ based on a dataset while maintaining privacy. We extensively compare our main algorithm to previous works in the same setting and show, both analytically and on experiments, that we outperform the state-of-the-art, significantly improving utility."

# Summary. An optional shortened abstract.
summary: ""

tags: ["Differential Privacy", "Data Analysis"]
categories: ["Differential Privacy", "Data Analysis"]
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf:
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
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

Currently, I'm updating the latest version to address reviewers’ comments and will soon release the full final paper.

We also have extensive code to reproduce all the results, in pure python and also notebooks to simplify understanding. So stay tuned!
