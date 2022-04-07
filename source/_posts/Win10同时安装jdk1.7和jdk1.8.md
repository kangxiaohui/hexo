---
title: 安装jdk7.x和8.x
categories: 技术
date: 2021-02-16 20:39:43
tags: win10
---

安装：

安装过程是傻瓜式安装，安装的路径根据自己的习惯进行选择。

<!--more-->

配置环境变量：

这里我们使用三个变量![image-20210216115344811](https://gitee.com/LYmystery/PicGo/raw/master/image/20210216115352.png)

 添加CLASSPATH，内容是：.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar

切换：

现在是%JAVA8_HOME%：![image-20210216115414101](https://gitee.com/LYmystery/PicGo/raw/master/image/20210216115415.png)

如果需要切换只需要更改JAVA_HOME中的变量8改为7就行了。![image-20210216115436652](https://gitee.com/LYmystery/PicGo/raw/master/image/20210216115438.png)

![image-20210216115503059](https://gitee.com/LYmystery/PicGo/raw/master/image/20210216115504.png)