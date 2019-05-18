---
layout:     post
title:      JVM运行时数据区域
subtitle:   JVM运行时数据区域
date:       2019年5月18日16:57:17
author:     dada
header-img: img/post-bg-kuaidi.jpg
catalog: true
tags:
    - JVM
---

### java虚拟机运行时数据区
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190518170720717.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNDQ2NzY4,size_16,color_FFFFFF,t_70)

> 	其中方法区、堆是线程共享的，而虚拟机栈、本地方法栈、程序计数器是线程隔离的。


### 程序计数器

	

> 程序计数器是一块较小的内存空间，他可以是看做当前线程所执行的字节码得到行号指示器，通过这个计数器的值来选取下一条需要执行
> 的指令、分支、循环、跳转、异常处理、线程恢复等基础功能都需要依赖这个计数器来完成。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190518172027744.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNDQ2NzY4,size_16,color_FFFFFF,t_70)

> 例: 当线程A执行到第二行,CPU切换到线程B的第1行，当线程B执行到第4行，CPU切换到线程A，需要通过这个程序计数器来确定要当前
> 线程执行的位置
