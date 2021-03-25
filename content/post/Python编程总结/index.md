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

### 写文件

```python
imwrite('temp.tif', data)
```

