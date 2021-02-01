---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "「论文阅读」- 重新审视时空相似性：一种面向交通流预测的深度学习框架"
authors: []
date: 2021-01-16T20:34:17+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2021-01-16T20:34:17+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: "AAAI 2019"

abstract: "Traffic prediction has drawn increasing attention in AI research field due to the increasing availability of large-scale traffic data and its importance in the real world. For example, an accurate taxi demand prediction can assist taxi companies in pre-allocating taxis. The key challenge of traffic prediction lies in how to model the complex spatial dependencies and temporal dynamics. Although both factors have been considered in modeling, existing works make strong assumptions about spatial dependence and temporal dynamics, i.e., spatial dependence is stationary in time, and temporal dynamics is strictly periodical. However, in practice the spatial dependence could be dynamic (i.e., changing from time to time), and the temporal dynamics could have some perturbation from one period to another period. In this paper, we make two important observations: (1) the spatial dependencies between locations are dynamic; and (2) the temporal dependency follows daily and weekly pattern but it is not strictly periodic for its dynamic temporal shifting. To address these two issues, we propose a novel Spatial-Temporal Dynamic Network (STDN), in which a flow gating mechanism is introduced to learn the dynamic similarity between locations, and a periodically shifted attention mechanism is designed to handle long-term periodic temporal shifting. To the best of our knowledge, this is the first work that tackle both issues in a unified framework. Our experimental results on real-world traffic datasets verify the effectiveness of the proposed method.
"

# Summary. An optional shortened abstract.
summary: "由于大规模交通数据的不断增加及其在现实世界中的重要性，交通预测在人工智能研究领域引起了越来越多的关注。例如，准确的出租车需求预测可以帮助出租车公司进行出租车的预分配。交通预测的关键挑战在于如何对复杂的空间依赖性和时间动态进行建模。虽然在建模中已经考虑了这两个因素，但现有的工作对空间依赖性和时间动态性做了很强的假设，即空间依赖性在时间上是静止的，而时间动态性是严格的周期性。然而，在实际工作中，空间依赖性可能是动态的(即在不同时期发生变化)，而时间依赖则可能从一个时期到另一个时期有一定的扰动。在本文中，我们提出了两个重要的观点。(1)地点之间的空间依赖性是动态的;(2)时间依赖性遵循日、周规律，但其动态时空变换并非严格的周期性。针对这两个问题，我们提出了一种新型的空间-时间动态网络(STDN)，其中引入了流门机制来学习位置之间的动态相似性，并设计了周期性转移注意力机制来处理长期周期性的时间转移。据我们所知，这是第一个在统一框架下解决这两个问题的工作。我们在真实世界的交通数据集上的实验结果验证了所提出的方法的有效性。
"

tags: []
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: revisiting-spatial-temporal-similarity-a-deep-learning-framework-for-traffic-prediction
url_code: https://github.com/tangxianfeng/STDN
url_dataset:
url_poster:
url_project:
url_slides: slice.pdf
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
