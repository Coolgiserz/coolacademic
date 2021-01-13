---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "认识数据驱动的测试"
subtitle: ""
summary: "测试的第X范式？"
authors: []
tags: [测试]
categories: [测试]
date: 2020-03-09T20:20:57+08:00
lastmod: 2020-03-09T20:20:57+08:00
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
projects: []
---
## 前言
之前的文章简单介绍了[自动化测试](../automated-testing-startup/)，在自动化测试平台中，有一个重要的组件或概念称为“数据驱动的测试（Data Driven Tests， DDT）”，其目的是将测试脚本与测试数据分离，本质上是测试逻辑的解耦，使得测试流程的代码编写与测试过程中所使用的数据/用例设计可以分别进行。

数据驱动的测试解决了如下痛点：
>对于同一份测试代码，测试数据可能会发生大量变化，如果测试数据与代码耦合可能会为代码维护带来不必要的麻烦或增加不必要的代码编写。

### 框架
以基于Python语言的[DDT](https://ddt.readthedocs.io/en/latest/)框架为例介绍DDT的主要模块功能与模块关系。

DDT主要有三大部件：
1. 数据源

    csv、excel、json、xml等

2. 数据加载脚本

    将数据源读取到内存中（特定的数据结构）

3. 测试脚本

    读取数据变量，进行测试，保存测试信息。

