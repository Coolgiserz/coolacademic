---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "面向Covid-19国内传播分析的人口流动网络分析"
summary: "数据战疫"
authors: []
tags: [COVID-19, 网络分析]
categories: [网络分析]
date: 2020-03-13T21:54:39+08:00
draft: false
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

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""
url_dataset: "https://www.datafountain.cn/datasets/130#"
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
### 数据集
#### 病例统计数据
- 丁香园统计的各地病例数

#### 移动性数据
- 百度迁徙

### 方法
#### 网络节点影响力排名
- PageRank
- HITS

#### 社区检测
- Newman 
- Ricci flow
- Infomap

### 案例分析
- 地级市人口流动网络节点影响力分析
- K感染数到达时间与城市节点影响力的相关性分析
- 网络社区发现

## 相关文献
- [Population flow drives spatio-temporal distribution of COVID-19 in China](https://www.nature.com/articles/s41586-020-2284-y)

- [Mobility network models of COVID-19 explain inequities and inform reopening](https://www.nature.com/articles/s41586-020-2923-3?fbclid=IwAR0iyWJwtGTAf19Uj4ikHG1VZPG221gFkt16zbH4-CbxjJOksp5MLS94EdU)

- [The effect of control strategies to reduce social mixing on outcomes of the COVID-19 epidemic in Wuhan, China: a modelling study](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(20)30073-6/fulltext)

    我们的预测显示，如果在4月初错峰复工，物理疏导措施最为有效；这使得2020年中期和2020年底的感染中位数分别减少了92%（IQR 66-97）和24%（13-90）以上。将这些措施持续到4月是有好处的，可以推迟和降低高峰期的高度、2020年底的中位数疫情规模，并为医疗系统提供更多的时间来扩大和应对。然而，物理距离措施的模型效果因传染性的持续时间和学童在流行病中的作用而不同。

- [Modeling and prediction of the 2019 coronavirus disease spreading in China incorporating human migration data](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0241171)

    本研究将每日城市间迁移数据与经典的易感-暴露-感染-清除（SEIR）模型进行整合，构建了适合描述中国2019年冠状病毒病（COVID-19）流行传播动态的新模型。从基于移动应用的人类迁徙追踪数据系统 "百度迁徙 "中采集了中国367个城市的每日城际迁徙数据。利用官方来源的感染病例、康复病例和死亡病例的早期疫情数据（2020年1月24日至2月16日）进行模型拟合。利用约束性非线性优化程序，对最佳数据拟合得到的模型参数集，用于估计随后几个月的疫情传播动态。该工作于2020年2月19日完成。我们的结果显示，中国大部分城市的感染人数将在2020年2月中旬至3月上旬达到高峰，武汉市、湖北省和中国其他地区的最终感染人数分别约为0.8%、不到0.1%和不到0.01%。此外，对于湖北省外和湖北省内的大部分城市（除武汉外），预计感染者总数将分别低于300人和4000人。