---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "硬盘分区的故事"
active: false
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-12-08T19:56:13+08:00
lastmod: 2020-12-08T19:56:13+08:00
featured: false
draft: true

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
- 为什么要进行硬盘分区？
- 各个分区有什么作用？
- 安装系统时应该如何分区？

## 分区
在使用Linux系统时，需要接触swap分区、boot分区、efi分区、home分区、/分区。
### swap分区
swap分区的功能就是在内存不够的情况下，操作系统先把内存中暂时不用的数据，存到硬盘的交换空间，腾出内存来让别的程序运行。
可以通过如下命令查看swap分区：
```shell
cat /proc/swaps
```
或者
```shell
top
```
设置swap分区大小其实就是创建一个一定大小的区域（文件）供内存交换使用
```shell
swapoff -a
swapon -a
sudo fallocate -l 30G /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
```
[如何在Ubuntu 16.04上增加Swap分区](https://blog.csdn.net/u010429286/article/details/79219230)

### efi分区

### boot分区

### 根目录

### home分区
Xorg:
[Xorg cpu占用问题，linux桌面系统致命伤（你的系统存在这个问题吗？)](https://forum.ubuntu.org.cn/viewtopic.php?t=324033)

备份电脑：

备份conda
```
conda env export > environment_py36.yml
```

压缩文件
```shell
tar -zcvf Projects.tar.gz Projects/
```
解压文件
```shell
tar -zxvf Project.tar.gz
```