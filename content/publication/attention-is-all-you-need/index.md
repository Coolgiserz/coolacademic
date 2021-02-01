---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "「论文翻译」- 你需要的只是注意力"
authors: []
date: 2020-09-30T19:09:30+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2021-01-14T19:09:30+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: "NIPS 2017"

abstract: "The dominant sequence transduction models are based on complex recurrent or convolutional neural networks that include an encoder and a decoder. The best performing models also connect the encoder and decoder through an attention mechanism. We propose a new simple network architecture, the Transformer, based solely on attention mechanisms, dispensing with recurrence and convolutions entirely. Experiments on two machine translation tasks show these models to be superior in quality while being more parallelizable and requiring significantly less time to train. Our model achieves 28.4 BLEU on the WMT 2014 English- to-German translation task, improving over the existing best results, including ensembles, by over 2 BLEU. On the WMT 2014 English-to-French translation task, our model establishes a new single-model state-of-the-art BLEU score of 41.0 after training for 3.5 days on eight GPUs, a small fraction of the training costs of the best models from the literature.
"

# Summary. An optional shortened abstract.
summary: "主流的序列推导模型是基于复杂的循环或卷积神经网络，它们包括一个编码器和一个解码器。性能最好的模型还通过注意机制连接编码器和解码器。我们提出了一种新的简单的网络架构--Transformer，完全基于注意力机制，完全不需要递归和卷积。在两个机器翻译任务上的实验表明，这些模型在质量上更胜一筹，同时可并行性更强，所需的训练时间也大大减少。我们的模型在WMT 2014英译德任务上实现了28.4 BLEU，比现有的最佳结果（包括合奏）提高了2 BLEU以上。在WMT 2014英语到法语翻译任务上，我们的模型在8个GPU上训练3.5天后，建立了一个新的单模型最先进的BLEU分数，达到41.0，这只是文献中最佳模型训练成本的一小部分。
"

tags: []
categories: [自然语言处理]
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: attention-is-all-you-need
url_code: https://github.com/tensorflow/tensor2tensor
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
### 引言
循环神经网络，特别是长短期记忆[12]和门控循环[7]神经网络，已经被牢固地确立为语言建模和机器翻译等序列建模和转换问题的最先进方法[29，2，5]。此后，大量的努力继续推动循环语言模型和编码器-解码器架构的边界[31，21，13]。

循环模型通常沿着输入和输出序列的符号位置进行因子计算。这种固有的顺序性使得我们无法训练实例中的并行化，这在较长的序列长度上变得至关重要，因为内存约束限制了跨实例的批处理。最近的工作通过因子化技巧[18]和条件计算[26]实现了计算效率的显著提高，同时也提高了后者情况下的模型性能。然而，顺序计算的基本约束仍然存在。

注意力机制已经成为各种任务中引人注目的序列建模和推导模型的一个组成部分，允许对依赖关系进行建模，而不考虑它们在输入或输出序列中的距离[2，16]。然而，除少数情况外[22]，这种注意机制是与循环网络一起使用的。

在这项工作中，我们提出了Transformer，一个摒弃递归的模型架构，而完全依靠注意力机制来绘制输入和输出之间的全局依赖关系。Transformer允许更多的并行化，并且在8个P100 GPU上训练12小时后，就可以在翻译质量上达到一个新的水平。

### 背景

减少顺序计算的目标也构成了扩展神经GPU[20]、ByteNet[15]和ConvS2S[8]的基础，它们都使用卷积神经网络作为基本构件，对所有输入和输出位置并行计算隐藏表示。在这些模型中，将两个任意输入或输出位置的信号关联起来所需的运算次数随着位置之间的距离而增长，对于ConvS2S来说是线性的，对于ByteNet来说是对数的。这使得学习遥远位置之间的依赖关系变得更加困难[11]。在Transformer中，这种情况被减少到了恒定的操作次数，尽管代价是由于注意力加权位置的平均化而降低了有效的分辨率，我们用多头注意力来抵消这种效果，如3.2节所述。

自注意力，有时也被称为内注意，是一种将单一序列的不同位置联系起来以计算序列表征的注意机制。自注意力已被成功地用于各种任务中，包括阅读理解、抽象总结、文本内涵和学习与任务无关的句子表征[4，22，23，19]。

端到端记忆网络是基于循环注意机制而不是序列排列的循环，已被证明在简单语言问题回答和语言建模任务中表现良好[28]。

然而，据我们所知，Transformer是第一个完全依靠自注意力来计算其输入和输出的表示，而不使用序列对齐的RNNs或卷积的转导模型。在下面的章节中，我们将描述Transformer，激励自注意力，并讨论其与[14，15]和[8]等模型相比的优势。

### 模型架构
![](images/fig1.png)

![](images/fig2.png)

### 结论
在这项工作中，我们提出了Transformer，这是第一个完全基于注意力的序列转换模型，用多头自注意力取代了编码器-解码器架构中最常用的循环层。

对于翻译任务，Transformer的训练速度可以显著快于基于循环层或卷积层的架构。在WMT 2014英译德和WMT 2014英译法两个翻译任务上，我们实现了新的技术状态。在前一个任务中，我们的最佳模型甚至超过了之前报道的所有合集。

我们对基于注意力的模型的未来感到兴奋，并计划将其应用于其他任务。我们计划将Transformer扩展到涉及文本以外的输入和输出模式的问题，并研究局部的、受限的注意力机制，以有效地处理图像、音频和视频等大型输入和输出。让生成的顺序性降低是我们的另一个研究目标。