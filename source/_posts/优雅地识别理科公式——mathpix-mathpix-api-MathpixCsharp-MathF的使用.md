---
title: 优雅地识别理科公式——mathpix/mathpix api/MathpixCsharp/MathF的使用
date: 2021-01-31 21:53:58
categories: 技术
tags: 软件
---

# 导读

最近有识别图片公式OCR识别地需求，发现Mathpix Snip甚合我意，只需要截个图，Mathpix Snip就可以将截图中的公式自动转化为 LaTex 代码表达式或者MS word格式（直接粘贴进word），我们只需要简单地修改就可以直接插入到LaTex或Word中，公式较为清晰规范的话是不需要修改的，电子公式的识别率几乎100%，而且可以识别手写的公式。

<!-- more-->

这是识别数学公式

![img](https://gitee.com/LYmystery/PicGo/raw/master/image/20210131215538.gif)

![img](https://gitee.com/LYmystery/PicGo/raw/master/image/20210131215600.png)

![img](https://gitee.com/LYmystery/PicGo/raw/master/image/20210131215626.png)

![img](https://gitee.com/LYmystery/PicGo/raw/master/image/20210131215635.png)

![img](https://gitee.com/LYmystery/PicGo/raw/master/image/20210131215644.jpg)

# Mathpix Snip介绍

说明：需注册，个人邮箱50条/月，Edu邮箱100条/月，可以保存历史记录，站里之前也有人推荐过。
官方网站：https://mathpix.com/
更多讨论：http://kuing.orzweb.net/viewthread.php?tid=6122

# MathpixCsharp项目介绍（推荐）

说明：需自己申请Mathpix api（需要Visa/MasterCard的信用卡验证），api请求限制1000条/月，无法保存历史记录，这是爱好者自己开发的工具，站里也没人推荐
项目网站：https://github.com/itewqq/MathpixCsharp
下载地址：https://github.com/itewqq/MathpixCsharp/releases



# MathF项目介绍（着重推荐，适合临时使用的小白）

说明：个人开发，也是利用了**mathpix**的接口，但是不需要注册账号申请api，也去掉了每月请求数的限制，无法保存历史记录，这是爱好者自己开发的工具，站里也没人推荐
在线网站：https://mathcode.herokuapp.com/
项目网站：https://github.com/itewqq/MathF

![img](https://gitee.com/LYmystery/PicGo/raw/master/image/20210131215744.jpg)

# Snipaste截图工具推荐

说明：由于Mathpix是基于截图的程序，故推荐Snipaste用以截图，当然你也可以选择其他熟悉的工具
官方网站：https://zh.snipaste.com/

![img](https://gitee.com/LYmystery/PicGo/raw/master/image/20210131215807.gif)

# 补充说明

为了鼓励支持原作者，这里都是贴出原作者发布地址，如果Github界面打不开，一般是个别电信运营商的域名DNS污染问题，可以尝试以下操作
1.修改本地DNS服务器为8.8.8.8;
2.打开 https://www.ipaddress.com/ 输入访问不了的域名，查询之后可以获得正确的 IP 地址;
3.在本机的 host 文件中添加，建议使用 SwitchHosts 方便 host 管理

```
199.232.68.133 raw.githubusercontent.com
199.232.68.133 user-images.githubusercontent.com
199.232.68.133 avatars2.githubusercontent.com
199.232.68.133 avatars1.githubusercontent.com
```

通过添加以上几条 host 配置，一般就正常了