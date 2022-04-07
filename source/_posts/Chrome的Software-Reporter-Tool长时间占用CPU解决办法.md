---
title: Chrome的Software Reporter Tool长时间占用CPU解决办法
categories: 技术
date: 2020-07-07 20:39:43
tags: chrome
---



## 什么是Software Reporter Tool

Software Reporter Tool是一个Chrome清理工具,用于清理谷歌浏览器中不必要或恶意的扩展，应用程序，劫持开始页面等等。当你安装Chrome时，Software_reporter_tool.exe也j就会被下载在SwReporter文件夹下的Chrome应用数据文件夹中。

<!-- more -->

## 如何关闭SRT

这个软件在运行的过程中可能会长时间地占用CPU，导致高CPU使用率。我们虽然可以通过任务管理器手动结束进程或者选择删除SRT，但这都不是长久的解决办法。因为前者过一段时间它又会再次运行，后者在浏览器更新的时候就又会重新被下载下来。要完美地解决这一个问题我们可以进入SRT目录，默认它位于以下目录

C:\Users\[YourName]\AppData\Local\Google\Chrome\User Data\SwReporter\[版本]\software_reporter_tool.exe

我们还可以通过`win+r`键打开运行命令窗口并输入以下命令快速找到它

%localappdata%\Google\Chrome\User Data\SwReporter



![](https://gitee.com/LYmystery/PicGo/raw/master/image/20200707204417.png)



- 右键单击software_reporter_tool.exe选择属性
- 转到“安全”选项卡
- 点击“高级”
- 点击“禁用继承”
- 选择"从此对象中删除所有继承的权限",之后一路点击“确定”“确定”。