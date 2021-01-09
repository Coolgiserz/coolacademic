---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "基于RFM和Kmeans的用户分群"
summary: "基于聚类分析的个性化营销"
authors: []
tags: [聚类, 机器学习, 个性化营销]
categories: [聚类, 个性化营销]
date: 2020-06-08T10:40:17+08:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: "https://github.com/Coolgiserz/NLP_starter/tree/master/CodePratices/MachineLearning/customer_segment_project"
url_pdf: ""
url_slides: ""
url_video: ""
url_dataset: "http://archive.ics.uci.edu/ml/datasets/online+retail"
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

## 前言
营销业务中比较重要的环节就是用户分群，其目的是做针对性、个性化的营销，而不是对每个用户都采用同样的营销。那么如何对用户进行分群就是一门值得研究的学问。

本项目实现经典的RFM用户分群模型，并用Kmeans对RFM特征进行聚类，作为探索个性化营销的初步尝试。

### RFM模型
RFM模型是经典的用户分群模型，从3个维度对用户进行分层。
> R: Recency, 表示用户最近一次购买的时间

> F: Frequency, 表示用户过去一段时间的购买次数

> M: Monetary, 表示用户过去一段时间内所花费的总金额

## 项目思路
### 步骤一：数据预处理

### 步骤二：特征提取
得到用户的R、F、M维度特征。

### 步骤三：用户分群
#### 法一：对RFM设置阈值对用户分群
对R、F、M三个维度的特征各自按照一定的阈值进行分组，分组有一定的原则。具体的阈值设置可以按照均值来分，也可以按照分位数，众数等作为划分的阈值。选择阈值之前可以先通过可视化探索用户各维度特征的分布特征。

分完组之后可以将每个组映射到一个类别，标明用户的“等级”或“价值”。通常认为：对于R而言，R越小用户价值越大；对于F而言，F越大用户价值越大；对于M而言，M越大用户价值越大。

将每个维度的等级进行综合可以对用户有一个综合评价，综合的方式有很多，最简单的可以是三个维度的加和。


#### 法二：基于聚类的用户分群

前面基于阈值的分群方法虽然简单容易操作，但是也过于一刀切，且对经验依赖较大。这里考虑对用户按照等级特征进行聚类实现用户分群。但该方法的缺点是对于每一个类簇需要人为地去解释，且如何确定类簇的个数也是一个问题。

## 资源小结
用户分群还可以基于很多特征进行，如活跃度、内容贡献、注册时间等.

- [腾讯移动分析-用户分群](https://mta.qq.com/docs/ctr_user_group.html)
- [读懂用户运营体系：用户分层和分群](http://www.woshipm.com/operate/598103.html)