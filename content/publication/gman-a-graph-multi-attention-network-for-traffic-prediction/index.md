---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "「论文阅读」—GMAN: 一种用于交通预测的图多注意力网络"
authors: []
date: 2020-12-23T11:25:09+08:00
doi: "10.1609/aaai.v34i01.5477"

# Schedule page publish date (NOT publication's date).
publishDate: 2020-12-23T11:25:09+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "AAAI Conference on Artificial Intelligence"
publication_short: "AAAI"

abstract: "Long-term traffic prediction is highly challenging due to the complexity of traffic systems and the constantly changing nature of many impacting factors. In this paper, we focus on the spatio-temporal factors, and propose a graph multi-attention network (GMAN) to predict traffic conditions for time steps ahead at different locations on a road network graph. GMAN adapts an encoder-decoder architecture, where both the encoder and the decoder consist of multiple spatio-temporal attention blocks to model the impact of the spatio-temporal factors on traffic conditions. The encoder encodes the input traffic features and the decoder predicts the output sequence. Between the encoder and the decoder, a transform attention layer is applied to convert the encoded traffic features to generate the sequence representations of future time steps as the input of the decoder. The transform attention mechanism models the direct relationships between historical and future time steps that helps to alleviate the error propagation problem among prediction time steps. Experimental results on two real-world traffic prediction tasks (i.e., traffic volume prediction and traffic speed prediction) demonstrate the superiority of GMAN. In particular, in the 1 hour ahead prediction, GMAN outperforms state-of-the-art methods by up to 4% improvement in MAE measure. The source code is available at this https URL."

# Summary. An optional shortened abstract.
summary: "由于交通系统的复杂性和诸多影响因素的不断变化，长期的交通预测具有很大的挑战性。本文主要针对时空因素，提出了一种图多注意力网络(GMAN)，用于预测路网图上不同位置前方时间步的交通状况。GMAN采用编码器-解码器架构，编码器和解码器均由多个时空注意力块组成，以模拟时空因素对交通状况的影响。编码器对输入的交通特征进行编码，解码器对输出序列进行预测。在编码器和解码器之间，应用转换注意力层对编码后的交通特征进行转换，生成未来时间步长的序列表示，作为解码器的输入。转换注意力机制模拟了历史时间步和未来时间步之间的直接关系，有助于缓解预测时间步之间的错误传播问题。在两个实际交通预测任务（即交通量预测和交通速度预测）上的实验结果证明了GMAN的优越性。特别是在1小时前的预测中，GMAN比最先进的方法在MAE测量方面的改进高达4%。源代码可在此https网址上获取。"

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

url_pdf: "gman-a-graph-multi-attention-network-for-traffic-prediction.pdf"
url_code: "https://github.com/zhengchuanpan/GMAN"
url_dataset: "https://drive.google.com/drive/folders/10FOTa6HXPqX8Pf5WRoRwcFnW9BrNZEIX?usp=drive_open"
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
