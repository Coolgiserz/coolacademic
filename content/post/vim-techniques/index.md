---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "人生苦短，我用Vim"
subtitle: ""
summary: "vim！win！"
authors: []
tags: []
categories: []
date: 2020-12-25T16:37:26+08:00
lastmod: 2020-12-25T16:37:26+08:00
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
## 如何配置强大的vim开发环境？
### 样式配置
代码高亮

### 编码工具
#### 代码补全

#### 括号补全

### 断点调试

## 有哪些必须记得的vim技巧？
### 目录浏览
##### 返回文件所在目录
可以使用```b#```返回到最后一个缓冲区，如果你只是打开一个文件，那么它会带你回到文件所在目录浏览
```:E```它很容易记住，并让你回到你打开的文件的目录列表。


##### 关闭窗口
```Ctrl+W c ```关闭当前窗口

### 分屏
#### 新建窗口
- split命令
- vsplit命令

#### 快捷键分屏
Ctrl+W s 水平分割当前打开的文件，相当于执行split省略文件名的命令
Ctrl+W v 垂直分割当前打开的文件，相当于执行vsplit省略文件名的命令

### 自动补全
CTRL+n 普通关键字
CTRL+n CTRL+x 当前缓冲区关键字
CTRL+x CTRL+i 文件关键字
CTRL+x CTRL+] 标签文件关键字
CTRL+x CTRL+k字典查找
CTRL+x CTRL+f 文件名补全
CTRL+x CTRL+o全能（Omni）补全

作者：鸿雁长飞光不度
链接：https://www.jianshu.com/p/c9563522b703
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

### 撤销修改
```u```

## 参考
- [把vim配置成顺手的python轻量级IDE（一）](https://www.jianshu.com/p/f0513d18742a)