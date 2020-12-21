---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "「论文阅读」-基于多任务深度学习的时空流预测方法"
authors: [CoolCats]
date: 2020-12-08T16:13:24+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2020-12-08T16:13:24+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: "TKDE"

abstract: ""

# Summary. An optional shortened abstract.
summary: "预测时空网络中的流量（如车辆、人群和自行车的流量），包括一个节点的进出流量和不同节点之间的转换，在交通系统中起着重要作用。然而，这是一个非常具有挑战性的问题，受多种复杂因素的影响，如不同地点之间的空间相关性，不同时间间隔之间的时间相关性，以及外部因素（如事件和天气）。此外，节点上的流量（称为节点流）和节点之间的过渡（边缘流）相互影响。为了解决这些问题，我们提出了一个多任务深度学习框架，同时预测整个时空网络的节点流和边缘流。基于全卷积网络，我们的方法设计了两个复杂的模型，分别用于预测节点流和边缘流。这两个模型通过耦合它们的中间层的潜伏表征来连接，并一起训练。外部因素也通过门控融合机制整合到框架中。在边缘流预测模型中，我们采用了一个嵌入组件来处理节点之间的稀疏过渡。我们基于北京和纽约市的出租车数据对我们的方法进行了评估。实验结果表明，我们的方法具有超越ConvLSTM、CNN和Markov Random Field等11种基准的优势。"

tags: []
categories: [论文阅读]
featured: false
draft: true
# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: flow-prediction-in-spatio-temporal-network-based-on-multitask-deep-learning.pdf
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
# Flow Prediction in Spatio Temporal Network Based on Multitask Deep Learning

影响交通流的要素有哪些？
- 空间依赖
- 时间依赖
- 外部因素

因此要进行交通流预测，需要处理以下关键问题
- 如何建模空间依赖？
- 如何建模时间依赖？
- 如何将有助于交通流预测的外部因素/知识融合到模型中？


## 参考资料
- [Multitask-Learning](https://github.com/mbs0221/Multitask-Learning)