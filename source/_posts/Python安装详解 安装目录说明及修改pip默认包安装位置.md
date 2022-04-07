---
title: Python安装详解
categories: 学习
date: 2021-02-26 20:39:43
tags: python
---

# 下载

  首先需要说明的是，Python 是开源跨平台的，不同系统下的安装区别较大。Python最新源码、安装包，新闻资讯等可以在Python的官网 https://www.python.org/ 查看到。你还可以在以上链接中下载 Python 的文档， HTML、PDF 和 PostScript 等格式的文档等等各种资料。

<!--more-->

![](https://img-blog.csdnimg.cn/201812131623025.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
从上面下载下来的默认为32位的，如果要下载64位的，这需要如下图进行查找
![](https://img-blog.csdnimg.cn/20181213162312639.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
点击对应版本后，会出现对应版本的详细介绍页面，将滚动条拉倒最后，就会发现针对各平台的下载文件
![](https://img-blog.csdnimg.cn/20181213162324123.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
这样就得到了 Python 的安装包了！

# Windows

下面重点介绍 Windows 下的安装。其他平台后续有用到在完善。

## 安装

直接双击安装包，就会出现以下界面
![](https://img-blog.csdnimg.cn/20181213162336828.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
其中，最好选择上 `Add Python xxx to PATH`，否则后续还得自己将 Python 添加到 Windows 的环境变量中。还有个默认选择的 `Install launcher for all users(recommended)`，这个也是有用的，尤其是在安装了不同版本的 Python 时。这个东西后面在详细说明。然后，直接点击`Customise installation`，出现如下界面
![](https://img-blog.csdnimg.cn/201812131623481.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
上面的界面中，默认所有内容都是被选择的。至于每个是啥意思，后面在详细介绍。这里默认全选即可，然后点击`Next`，出现如下界面
![](https://img-blog.csdnimg.cn/20181213162355678.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
其中的， `install for all user` 最好选择，选择后 `Precompile standard library` 将自动被选择，之后点击 `Install`，等待安装完成就好了！安装完成后，效果图如下
![success](https://img-blog.csdnimg.cn/20181213162408651.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
如果在开始安装时，没有选择将 Python 添加到环境变量，则按住后需要自己手动添加上图所示的环境变量！

> 注意如果是第一次安装，安装完成后会有个提示 `Removing the MAX_PATH Limitation`。我们选择`Enable`即可。最新的 3.9.0 如下所示（貌似与之前版本的描述不一致了，之前是 Enable 现在是 Disable）：
> ![](https://img-blog.csdnimg.cn/20201008070618963.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70#pic_center)
> 主要原因是 Windows historically has limited path lengths to 260 characters. This meant that paths longer than this would not resolve and errors would result.
> 也可以手动修改注册表`HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem@LongPathsEnabled to 1.`

# 安装目录介绍

在执行完以上步骤之后，就会在自己指定的目录下生成各种安装后的文件，目录结构如下：
![Dir](https://img-blog.csdnimg.cn/20181214080209657.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
下面简单介绍一下个目录/文件的具体用途：

- **DLLs：** Python 自己使用的动态库
- **Doc：** 自带的 Python 使用说明文档（如果上面安装时不选择，应该会没有，这个没具体试过）
- **include：** 包含共享目录
- **Lib：** 库文件，放自定义模块和包
- **libs：** 编译生成的Python 自己使用的静态库
- **Scripts：** 各种包/模块对应的可执行程序。安装时如果选择了pip。那么pip的可执行程序就在此！
- **tcl：** 桌面编程包

# 修改 PIP 默认安装位置

## 问题

上面在安装时，选择了安装pip（***注意：从3.4版本之后，pip才开始为默认组件，之前的版本是没有的*** ）。后面我们就可以使用pip安装各种自己使用的包了。但是，如果不进行配置，默认安装位置如下所示：
![](https://img-blog.csdnimg.cn/20181214083018571.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
默认安装位置是`C:\Users\ZCShou\AppData\Roaming\Python\Python37\Scripts`。***个人更倾向于不把这些东西放到系统盘，而是放到 Python 自己的安装目录的对应的子目录中！***

## 修改

首先，使用如下命令`python -m site` 查看
![](https://img-blog.csdnimg.cn/20181214083722400.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
***这里的`USER_BASE`和`USER_SITE`其实就是默认的启用Python通过pip自动下载的脚本和依赖安装包的基础路径。*** 接着使用命令`python -m site -help`，便会看到如下：
![](https://img-blog.csdnimg.cn/20181214084202385.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
以上说明了，路径的配置是在我们安装目录下的`lib\site.py`这文件中进行配置的！那么接下来修改这个文件就可以了！
![](https://img-blog.csdnimg.cn/20181214084814547.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)
这里的`USER_BASE` 需要特殊注意：***其会自动在指定的路径后面添加`/Python37/Scripts`（和自己的安装路径有关），有强迫症的自己注意！*** 然后再次使用命令查看

```c
C:\Users\ZCShou>python -m site
sys.path = [
    'C:\\Users\\ZCShou',
    'D:\\Program Files\\Python37\\python37.zip',
    'D:\\Program Files\\Python37\\DLLs',
    'D:\\Program Files\\Python37\\lib',
    'D:\\Program Files\\Python37',
    'D:\\Program Files\\Python37\\Lib\\site-packages',
]
USER_BASE: 'D:\\Program Files' (exists)
USER_SITE: 'D:\\Program Files\\Python37\\Lib\\site-packages' (exists)
ENABLE_USER_SITE: True
123456789101112
```

此后重新安装自己使用的包就可以了。这样新安装的包的可执行文件就会位于 Python 目录下的 `Scripts` 目下，包即会被放到 Python 目录下`lib\site-packages`目录下了！
![](https://img-blog.csdnimg.cn/20181214090650517.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)

# pip 升级

有上面的图片可知，默认安装Python 3.7.1 版本后，其自带的pip版本过低，总是提示升级！升级命令提示中已经给出，直接执行即可！
![](https://img-blog.csdnimg.cn/20181214092020389.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1pDU2hvdUNTRE4=,size_16,color_FFFFFF,t_70)