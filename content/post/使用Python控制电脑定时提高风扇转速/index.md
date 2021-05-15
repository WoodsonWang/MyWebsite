---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "使用Python控制电脑定时提高风扇转速"
subtitle: ""
summary: ""
authors: [码小点]
tags: []
categories: []
date: 2021-05-16T03:30:07+08:00
lastmod: 2021-05-16T03:30:07+08:00
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



## 起因

​		最近使用笔记本进行挖矿，放在屋子里，白天若是全力散热的话噪音会比较大，想晚上定时提高风扇转速，白天就静音挖矿。

## 使用Python模拟点击

​		没有找到控制windows风扇的python包，就想着我的笔记本是机械革命，内部自带了修改工作模式提高风扇转速的软件，所以使用python进行定时模拟鼠标点击软件中的按钮即可实现风扇的调节。

## 代码

### python包

```python
pip install PyUserInput
```

### 鼠标点击

```python
from pykeyboard import *
from pymouse import *
import time
import logging

mouse = PyMouse()
# button 1是左键，2是右键
mouse.click(control_pos[0],control_pos[1],button=2)
```



### 打印日志到文件

```python
logging.basicConfig(level=logging.DEBUG,#控制台打印的日志级别
                    filename='new.log',
                    filemode='a',##模式，有w和a，w就是写模式，每次都会重新写日志，覆盖之前的日志
                    #a是追加模式，默认如果不写的话，就是追加模式
                    format=
                    '%(asctime)s - %(pathname)s[line:%(lineno)d] - %(levelname)s: %(message)s'
                    #日志格式
                    )
```

代码中

```python
logging.info("{}打开风扇到100%".format(current_time_minute))
```



## 参考

1. [pykeyboard ,pymouse 操作键盘和鼠标](https://www.cnblogs.com/jodie2019/p/12313472.html)
2. [PyMouse、PyKeyboard用python操作鼠标和键盘](https://www.cnblogs.com/zjutlitao/p/10188434.html)
3. [python获取当前时间](https://www.runoob.com/python/python-date-time.html)
4. [log打印日志](https://www.cnblogs.com/nancyzhu/p/8551506.html)

