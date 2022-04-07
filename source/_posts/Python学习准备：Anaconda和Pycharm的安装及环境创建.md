---
title: Python学习准备：Anaconda和Pycharm的安装及环境创建
categories: 学习
date: 2021-02-14 20:39:43
tags: python
---

# Python学习准备：Anaconda和Pycharm的安装及环境创建

[转载]: https://blog.csdn.net/qq_38549200/article/details/80695111

## 一、Anaconda

#### 1. **Anaconda是什么？**

   [Anaconda](https://www.continuum.io/why-anaconda)是一个用于科学计算的Python发行版，支持 Linux, Mac, Windows系统，提供了包管理与环境管理的功能，可以很方便地解决多版本python并存、切换以及各种第三方包安装问题。Anaconda利用工具/命令`conda`来进行package和environment的管理，并且已经包含了Python和相关的配套工具。 

**conda** 是开源包（packages）和虚拟环境（environment）的管理系统。

<!--more-->

#### 2. **Anaconda的安装**

​    首先，下载安装包。Anaconda的下载方式有两种：

   通过官网下载，选择适合自己的电脑版本的安装包。https://www.anaconda.com/download/

   在官网中下载比较缓慢，可以通过清华大学开源软件镜像站下载。

   [https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/](https://link.jianshu.com/?t=https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/)

   双击Anaconda的安装包，按照如下步骤安装：

   ![img](https://img-blog.csdn.net/2018061417045842?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

  ![img](https://img-blog.csdn.net/20180614170513219?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

  因为是自己的笔记本，我选择的是对于全部用户都行，这个看自己的需要。

  ![img](https://img-blog.csdn.net/20180614170522907?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

我在安装过程中，因为懒得专门配环境变量，就直接勾选了添加环境变量

  ![img](https://img-blog.csdn.net/20180614170652122?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

  ![img](https://img-blog.csdn.net/20180614170848414?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

 ![img](https://img-blog.csdn.net/20180614170911749?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

 ![img](https://img-blog.csdn.net/20180614170928141?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

 安装成功。如果是windows用户，可以打开命令窗口，输入'python'，看看是否成功安装

![img](https://img-blog.csdn.net/20180614171035541?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

打开Anaconda文件

![img](https://img-blog.csdn.net/20180614171133524?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)





 

**Anaconda Cloud** 是管理公共或者私有python notebook、conda、环境和packages的地方，可以方便分享和追踪。

**Anaconda Navigator** 是Anaconda可视化的管理界面。

**Anaconda Prompt** 是一个Anaconda的终端，可以便捷的操作conda环境。

**Jupyter Notebook** 这得从IPython 3.x版本开始说起，这是最后的大一统版本，包括notebook、qtconsole等等，从IPython4.0版本开始IPython只集中精力做交互式shell，变得轻量化，而剩下的notebook格式，qtconsole，和notebookweb应用等都分离出来统一命名为Jupyter。至此IPython和Jupyter分家。

**JupyterQtconsole** 调用交互式命令台。从IPython4.0版本开始，很多IPython子命令现在变成了Jupyter子命令，如ipython notebook现在是jupyter noteboook。

**ipython**是一个python的交互式shell，比默认的pythonshell好用得多，支持变量自动补全，自动缩进，支持bash shell命令，内置了许多很有用的功能和函数。学习ipython将会让我们以一种更高的效率来使用python。同时它也是利用Python进行科学计算和交互可视化的一个最佳的平台。

**Spyder** 是一个使用Python语言的开放源代码跨平台科学运算IDE，是一种简单的集成开发环境。Spyder可以跨平台，也可以使用附加组件扩充，自带交互式工具以处理数据。

## 二、Pycharm

 配置完Anaconda之后，其实已经可以用已经安装好的ipython、spyder写代码了，但是个人感觉Pycharm很好用，基本上的代码都在Pycharm上敲的，所以也就把安装过程记录下来了。

**1.Pycharm的安装**

下载安装包，这个直接在官网上下载就好。http://www.jetbrains.com/pycharm/download/#section=windows

按照步骤走

![img](https://img-blog.csdn.net/20180614173146210?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

自己设置的路径

![img](https://img-blog.csdn.net/20180614173201435?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20180614173238714?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20180614173249632?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20180614173302699?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

安装完成，使用时会结合第三部分环境搭建来讲



## 三、使用conda建立运行环境

 这里直接写搭建过程需要的代码.



#### 1.搭建一个名叫scikit-learn的环境

windows系统进入‘运行’界面，输入'cmd'，确定

（1）conda env list      #显示已经存在的环境

![img](https://img-blog.csdn.net/20180615165850987?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)   

（2）conda create -n scikit-learn python  #创建环境

（3）y  回车

（4）activate scikit-learn          #进入环境

（5）conda list                 #查看环境中存在的包

（6）pip install ......              #安装包

（7）deactivate                 #退出环境



#### 2.将搭建好的scikit-learn环境配置到Pycharm中，开始编程

（1）双击Pycharm，点击创建新项目

（2）选择创建项目的位置及项目名字，选择“Existing interpreter”

![img](https://img-blog.csdn.net/20180615171609500?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

（3）按如下步骤选择路径，找到刚刚已经配置好的环境

![img](https://img-blog.csdn.net/20180615171634632?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20180615171159254?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20180615171244526?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20180615171340101?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20180615171700928?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

（4）创建成功

![img](https://img-blog.csdn.net/20180615171804203?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

（5）新建一个py文件，就可以愉快地写代码了。

![img](https://img-blog.csdn.net/20180615171906565?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20180615172058853?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NTQ5MjAw/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

写在后面的话：

   自己的第一篇博客算是写完了，很基础，希望能给刚入门的朋友们一点启示，少走一些弯路。想起自己刚接触python的时候，自己甚至都不知道在哪里敲代码，对于什么Ipython,spyder,pycharm更是一头雾水，在慢慢探索中，终于找到自己喜欢的编译器。在使用Pycharm中，一度也不知道怎么配置自己已经创建好的环境。故此，趁着这次机会把细节写出来，希望今后的自己也能不断学习，持续更新~~

   文中若有不当之处，欢迎大家批评指正~~