---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Sklearn使用"
subtitle: ""
summary: "Sklearn常用方法"
authors: [码小点]
tags: [Python]
categories: [编程]
date: 2021-04-20T21:57:49+08:00
lastmod: 2021-04-20T21:57:49+08:00
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


<script async src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js"></script>

<span id="busuanzi_container_site_pv" style="color:#829fbc;font-size:14px">本站总访问量 :eyes:<span id="busuanzi_value_site_pv"></span>次</span>

{{< toc summary="目录">}}



## 数据打乱

```python
x, y = sklearn.utils.shuffle(X, Y,random_state=1)
```

## 数据归一化

### 最大最小值归一化

```python
from sklearn.preprocessing import MinMaxScaler
data = [[-1, 2], [-0.5, 6], [0, 10], [1, 18]]
scaler = MinMaxScaler()
print(scaler.fit_transform(data))
```

## 混淆矩阵

![image-20210430131520633](image-20210430131520633.png)

