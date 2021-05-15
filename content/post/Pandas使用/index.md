---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Pandas使用"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2021-04-27T16:59:23+08:00
lastmod: 2021-04-27T16:59:23+08:00
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



# 读取csv

```python
data1=pd.read_csv=("test.csv")#自动把第一行作列属性，第一行不能用
data2pd.read_csv("test.cvs",header=None)#不把第一行作列属性
```

## 保存进CSV

```python
# encoding 设置中文防止乱码
df.to_csv(file,index=False,encoding='utf_8_sig')
```



