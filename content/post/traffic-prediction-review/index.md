---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "交通流预测总结"
subtitle: ""
summary: "入门交通流预测应该知道的事儿"
authors: []
tags: []
categories: []
date: 2020-12-12T22:22:01+08:00
lastmod: 2020-12-12T22:22:01+08:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: ["awesome-traffic-prediction"]
---
# 交通流预测
## 背景介绍
### 交通流预测有何意义？
交通流预测包括道路交通状况（速度、流量等）估计、行程到达时间估计，对人们的生活具有重要意义。

对于广大普通群众来说，你可以依赖交通流预测工具来通知亲朋好友你是否有可能会迟到，也可以依据路况信息为重要会议的出发时间点作合理规划：不至于迟到也不至于过早出发而空空等待。
对于商业公司来说，如共享单车/出租车公司可以依据区域交通状况规划车源的分配，达到最大的收益和效率。

### 如何进行交通流预测？
依赖的是什么数据？路段的在线交通数据

#### 影响交通流的因素有？
但想要准确地估计交通状况会遇到一些困难。
- 交通流存在一些如周期性、趋势性的模式，并且这种模式是存在波动性的；

  如：尽管每个早上晚上都会有交通高峰期，但高峰期出现的准确时间会有很大波动

- 道路之间的交通情况存在空间依赖性；

  一条道路的交通状况会影响周围路段的交通状况

- 多种外部因素会影响交通情况；

  如道路质量、速度限制、事故、道路关闭等外部因素对交通流预测有所影响，增加了交通流预测模型的复杂性。

#### 交通流预测最关键的问题是？
##### 假设数据质量较高

- 如何建模路段交通流之间的空间依赖性？

- 如何建模历史交通流的时序模式？

- 哪些外部因素会影响交通状况，如何将这些因素融合到交通流预测模型中？

##### 假设数据质量不足
除了上面几个问题以外，还需要考虑数据收集不全或者有噪声的情形。
- 如何评价交通流数据的质量？

- 如何从有噪声的数据中准确地预测交通状况？

- 如何进行交通流数据补全？

#### 如何评价交通流预测的效果？

## 学习资料
[How to Predict Severe Traffic Jams with Python and Recurrent Neural Networks?](https://towardsdatascience.com/how-to-predict-severe-traffic-jams-with-python-and-recurrent-neural-networks-e53b6d411e8d)

[Time series forecasting-Tensorflow Tutorial](https://www.tensorflow.org/tutorials/structured_data/time_series)