---
title: 国内访问Github
categories: 技术
date: 2021-05-21 15:06:55
tags: github
---
无法打开GitHub的解决办法
在解决这以问题之前，我们需要了解一下知识点：

在网络上访问网站，要首先通过DNS服务器把网络域名（www.XXXX.com）解析成形如XXX.XXX.XXX.XXX的IP地址后，我们的计算机才能访问。
例如：网络域名：https://github.com 对应的IP地址为：140.82.114.3

根据Windows系统规定，在进行DNS请求以前，Windows系统会先检查自己的Hosts文件中是否有这个地址映射关系，如果有则调用这个IP地址映射，如果没有再向已知的DNS 服务器提出域名解析。也就是说Hosts的请求级别比DNS高。

下面就通过在系统中文件hosts中添加域名和IP地址的映射关系，来解决这一问题：

1.首先确定github网站的IP:
打开：https://github.com.ipaddress.com
可以查看到github.com对应的IP为：140.82.114.3

2.确定域名的IP:
打开：https://fastly.net.ipaddress.com/github.global.ssl.fastly.net
可以查看到github.global.ssl.fastly.net对应的IP为：199.232.5.194

3.确定静态资源的IP:
打开：https://github.com.ipaddress.com/assets-cdn.github.com
可以查看到

找到这些域名对应的IP之后，将其添加到hosts文件中（位置：C:\Windows\System32\drivers\etc），找到hosts文件，用记事本打开，在文本的最后添加：
140.82.114.3 github.com
140.82.114.3 www.github.com
199.232.5.194 github.global.ssl.fastly.net
185.199.108.153 github.github.io
185.199.109.153 github.github.io
185.199.110.153 github.github.io
185.199.111.153 github.github.io
注意：这里的对应关系是静态的，当对应关系改变之后，需要再次查看该对应关系，手动在hosts文本中修改。保存之后，即可打开github.

修改完hosts文件后 在cmd中执行 ipconfig /flushdns 生效。