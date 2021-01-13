---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "「论文阅读」- Incrementally Improving Graph Wavenet Performance"
authors: []
date: 2021-01-10T19:03:57+08:00
doi: ""
draft: true
# Schedule page publish date (NOT publication's date).
publishDate: 2021-01-10T19:03:57+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["0"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "We present a series of modifications which improve upon Graph WaveNet’s previously state-of-the-art performance on the METR-LA traffic prediction task. The goal of this task is to predict the future speed of traffic at each sensor in a network using the past hour of sensor readings. Graph WaveNet (GWN) is a spatio-temporal graph neural network which interleaves graph convolution to aggregate information from nearby sensors and dilated convolutions to aggregate information from the past. We improve GWN by (1) using better hyperparameters, (2) adding connections that allow larger gradients to flow back to the early convolutional layers, and (3) pretraining on an easier short-term traffic prediction task. These modifications reduce the mean absolute error by .06 on the METR-LA task, nearly equal to GWN’s improvement over its predecessor. These improvements generalize to the PEMS-BAY dataset, with similar relative magnitude. We also show that ensembling separate models for short-and long-term predictions further improves performance. Code is available at https://github.com/sshleifer/ Graph-WaveNet."

# Summary. An optional shortened abstract.
summary: "我们介绍了一系列的修改，这些修改改进了Graph WaveNet在METR-LA流量预测任务上的最新性能。该任务的目标是利用过去一小时的传感器读数来预测网络中每个传感器的未来流量速度。图波网(GWN)是一种时空图神经网络，它交织了图卷积来汇总附近传感器的信息，以及稀释卷积来汇总过去的信息。我们通过（1）使用更好的超参数，（2）增加连接，允许更大的梯度流回早期卷积层，以及（3）在一个更容易的短期交通预测任务上进行预训练来改进GWN。这些修改使METR-LA任务的平均绝对误差降低了0.06，几乎等于GWN对其前代的改进。这些改进可以推广到PEMS-BAY数据集上，相对幅度也差不多。我们还表明，对短期和长期预测的单独模型进行合集可以进一步提高性能。代码可在https://github.com/sshleifer/ Graph-WaveNet。"

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

url_pdf: incrementally-improving-graph-wavenet-performance
url_code: https://paperswithcode.com/paper/incrementally-improving-graph-wavenet
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
