---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "串口通信小结"
subtitle: ""
summary: "上位机与下位机的对话"
authors: []
tags: [嵌入式开发]
categories: []
date: 2020-02-19T20:27:56+08:00
lastmod: 2020-02-19T20:27:56+08:00
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
接触的一个智能门锁项目涉及到嵌入式设备的调试，本文简单总结串口通信相关知识，回答如下问题：
- 什么是上位机、下位机？
- 上位机与下位机之间如何通信？
- 如何进行串口通信？



