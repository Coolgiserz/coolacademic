---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "「论文阅读」- 一种基于时空图神经网络的出行时间估计解决方案"
authors: []
date: 2021-01-14T20:34:52+08:00
doi: "10.1145/3394486.3403320"

# Schedule page publish date (NOT publication's date).
publishDate: 2021-01-14T20:34:52+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["0"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: "KDD 2020"

abstract: "The task of travel time estimation (TTE), which estimates the travel time for a given route and departure time, plays an important role in intelligent transportation systems such as navigation, route planning, and ride-hailing services. This task is challenging because of many essential aspects, such as traffic prediction and contextual information. First, the accuracy of traffic prediction is strongly correlated with the traffic speed of the road segments in a route. Existing work mainly adopts spatial-temporal graph neural networks to improve the accuracy of traffic prediction, where spatial and temporal information is used separately. However, one drawback is that the spatial and temporal correlations are not fully exploited to obtain better accuracy. Second, contextual information of a route, i.e., the connections of adjacent road segments in the route, is an essential factor that impacts the driving speed. Previous work mainly uses sequential encoding models to address this issue. However, it is difficult to scale up sequential models to large-scale real-world services. In this paper, we propose an end-to-end neural framework named ConSTGAT, which integrates traffic prediction and contextual information to address these two problems. Specifically, we first propose a spatial-temporal graph neural network that adopts a novel graph attention mechanism, which is designed to fully exploit the joint relations of spatial and temporal information. Then, in order to efficiently take advantage of the contextual information, we design a computationally efficient model that applies convolutions over local windows to capture a route's contextual information and further employs multi-task learning to improve the performance. In this way, the travel time of each road segment can be computed in parallel and in advance. Extensive experiments conducted on large-scale real-world datasets demonstrate the superiority of ConSTGAT. In addition, ConSTGAT has already been deployed in production at Baidu Maps, and it successfully keeps serving tens of billions of requests every day. This confirms that ConSTGAT is a practical and robust solution for large-scale real-world TTE services"

# Summary. An optional shortened abstract.
summary: "给定出发时间和路线，预估行程时间在智能交通系统中发挥着重要的作用。首先，预测的准确性和各路段中的速度密切相关。现有的很多工作采用了时空图神经网络来提高交通预测的准确性，但是大部分的时空信息是分开使用的。这样的模型的缺点是没有充分利用时间和空间的相关性。其次，路线中的上下文信息，即路线中相邻的路段是影响车速的必要原因。先前的工作使用顺序编码模型来解决这个问题，但是很难将顺序模型扩展到大规模实际应用。在本文中，提出了ConSTGAT框架，该框架集成了流量预测和上下文信息以解决这两个问题。具体来说，首先提出一种时空图神经网络，该网络采用一种新颖的图注意力机制，旨在充分利用时空信息的联合关系。然后，为了有效利用上下文信息，该模型在局部窗口上采用卷积操作以捕获路线的上下文信息，并进一步采用多任务学习来提高性能。以此方式，可以并行并预先计算每个路段的行驶时间。最后在真实世界数据集上进行的大量实验证明了ConSTGAT的优越性。此外，ConSTGAT已经在百度地图上进行了部署，它每天成功地满足数百亿个请求。这证实了ConSTGAT是针对大型现实世界TTE服务的实用且强大的解决方案。"

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

url_pdf: ConSTGAT-contextual-spatial-stemporal-graph-attention-network-for-travel-time-estimation-at-baidu-maps
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source: https://mp.weixin.qq.com/s?__biz=Mzg4MTE4ODQ3MA==&mid=2247490440&idx=1&sn=ad6319b2d5f1585c6275f0ee93ed33fc&chksm=cf689091f81f1987c7445638ffc397d391c663b3c5ceeaec55552372204b7487cf07351fd458&cur_album_id=1427682206876794881&scene=189#rd
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
