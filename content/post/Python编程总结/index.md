---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Python编程总结"
subtitle: ""
summary: "总结python常用函数"
authors: []
tags: []
categories: []
date: 2021-03-12T14:13:25+08:00
lastmod: 2021-03-12T14:13:25+08:00
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



1. [Python操作配置文件](https://blog.csdn.net/Demo_3/article/details/78275389?utm_medium=distribute.pc_relevant.none-task-blog-searchFromBaidu-8.control&dist_request_id=&depth_1-utm_source=distribute.pc_relevant.none-task-blog-searchFromBaidu-8.control)

## tifffile

pip install tifffile

[网站](https://pypi.org/project/tifffile/)

读写tif文件

### 读文件

```python
import tifffile

img = tifffile.imread(file)
```

### 写入

```python
imwrite('temp.tif', data)
```

## libtiff

### 写入

```python
from libtiff import TIFF

tif = TIFF.open(path, 'w')
tif.write_image(image)
```

## CV2

### 保存文件

```python
import cv2

cv2.imwrite('result_label_cv2.tif',img_arr)
```

### 读取文件

```python
img = cv2.imread ('C:/Users/Administrator/Pictures/test1.jpg')
```



## numpy

### 矩阵合并

一维矩阵合并

```python
a = np.array([1,2,3,4,5,5])
c = np.array([2,3,4,54,5])
d = np.concatenate((a,c))
print(d)

[ 1  2  3  4  5  5  2  3  4 54  5]
```

### 改变矩阵形状

展成一维

```python
img1_pred = cv2.imread(f1_pred)
img1_pred = img1_pred.flatten()
```

