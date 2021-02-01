---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "「论文阅读」- T-MGCN时间多图卷积网络用于交通流预测"
authors: []
date: 2021-01-14T20:29:49+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2021-01-14T20:29:49+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transaction on Intelligent Transpotation System"
publication_short: "TITS"

abstract: ""

# Summary. An optional shortened abstract.
summary: "由于复杂的空间和时间相关性，交通流预测一直是一项具有挑战性的任务。现有的工作试图通过开发各种时空模型来解决这一问题。然而，我们观察到遥远道路之间的语义关联性对于交通流预测也是至关重要的。为了将路网中的空间、时间、语义关联与各种全局特征联合建模，本文提出了T-MGCN (Temporal Multi-Graph Convolutional network)交通流预测深度学习框架。首先，识别了几种不同类型的语义关联，并将道路间的非欧氏空间关联和异构语义关联编码到多个图中，通过多图卷积网络对关联性进行建模。然后利用循环神经网络学习交通流的动态模式，以捕获时间相关性。最后利用全连接神经网络融合时空相关性和全局特征。"

tags: []
categories: [智慧交通]
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: temporal-multi-graph-convolutional-network-for-traffic-flow-prediction
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source: https://mp.weixin.qq.com/s/Coymoc2YZpaUTeh5PPYXkg
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

## 参考
https://mp.weixin.qq.com/s/Coymoc2YZpaUTeh5PPYXkg