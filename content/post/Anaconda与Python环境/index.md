---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Anaconda与Python环境"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2021-03-17T19:56:13+08:00
lastmod: 2021-03-17T19:56:13+08:00
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



{{<toc summary="目录">}}





## 创建新环境

```csharp
conda create -n 环境名称 python=3.7
```

## 删除环境

```csharp
conda remove -n 环境名称 --all
```

## 查看环境和位置

```csharp
conda info --envs
```

## 包安装
### 网络安装
```csharp
pip install 包名

conda install 包名
```

### 本地安装

网络上下载python包，使用pip安装
```csharp
pip install 包名
```

[python包下载地址1](https://www.lfd.uci.edu/~gohlke/pythonlibs/)

