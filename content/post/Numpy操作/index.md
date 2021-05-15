---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Numpy操作"
subtitle: ""
summary: "
numpy总结操作

"
authors: [码小点]
tags: 
categories: 
- 教程
- Python
date: 2021-03-08T11:49:34+08:00
lastmod: 2021-03-08T11:49:34+08:00
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



## 计算

### 计算矩阵行列式

```python
numpy.linalg.det(a)
```

### 平方 乘方 平方根

```python
numpy.square()  pow(x, x)  numpy.sqrt()
```

### 以e为底的对数

```python
np.log(x)
```

### 对数

以2为底的对数

```python
import math
math.log(8,2) # 以2为底8的对数
import numpy as np
np.log2(8)
```

以自然对数e为底

```python
import math
math.log(8,math.e) # 以2为底8的对数
import numpy as np
np.log(8)
```



## 保存

### 多个数组保存到一个文件

```python
import numpy as np
a=np.arange(3)
b=np.arange(4)
c=np.arange(5)
np.savez('array_save.npz',a,b,c_array=c)

A=np.load('array_save.npz')
print(A['arr_0'])
print(A['arr_1'])
print(A['c_array'])
```

### 保存到未压缩的npy文件中

```python
import numpy as np
a=np.arange(5)
np.save('test.npy',a)

a=np.load('test.npy')
print(a)
```

## 维度

### 变成一维

```python
a=arr1.flatten() 
```

### 除最后一个维度外，其他展成1维

```python
a = np.reshape(a,(-1,a.shape[-1]))
```

## 转为numpy数组

### asarray()

将原数组转为numpy，不对原数组拷贝，原数组改变，新numpy改变

### array()

对原数组进行拷贝，原数组改变，新numpy不改变

