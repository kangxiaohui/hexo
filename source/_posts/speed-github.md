---
title: 加速访问Github
categories: 技术
date: 2020-02-26 15:06:55
tags: github
---
# 说一下访问慢的原因

1. 由于 github.com 网站位于美国旧金山,所以初始访问 github.com 时网络寻址会比较耗费时间,这是网站打开速度慢的其中一个原因.
2. 最初用户从浏览器中输入 github.com 网址时,浏览器并不知道这个域名对应的真实 ip 地址,先问问自己电脑认识不认识这个域名的门牌号,如果本机不认识会接着往上问,当地运行商也不认识这个域名的话,继续问上级,直到问出来 github.com 的门牌号是 192.30.253.113 为止!如此繁琐的问路过程被称之为 DNS 寻址,如果问路的时间都占用很久,那么访问网站的速度自然会很慢.

## 主域名和多个子域名

正常来说,网站的主域名下会存在多个子域名,由这些域名组合在一起提供完整的服务.

而 github.com 也不例外,其中 github.com是一级域名,也是主域名,其他的域名基本上都是二级域名或者说次域名. 所以我们不仅要告诉本机 github.com 的主域名,还要把相关的子域名也告诉本机,帮人帮到底,送福送到西! 那到哪里去查询域名和 ip 的对应关系呢?

<!-- more -->

## 推荐几个查询域名解析的网站

1. [https://www.ipaddress.com/](https://www.ipaddress.com/)
2. [http://tool.chinaz.com/dns/](http://tool.chinaz.com/dns/)

## 体验域名查询
根据查到的相关域名信息,再次查询出这些域名对应的 ip 地址,于是整理出以下内容.
```
#github related website
192.30.253.113 github.com
199.232.5.194 github.global.ssl.fastly.net
192.30.253.119 gist.github.com
192.30.253.120 nodeload.github.com
199.232.28.133 raw.github.com
140.82.113.17 training.github.com
192.30.253.113 www.github.com
99.232.68.133 avatars0.githubusercontent.com
199.232.68.133 avatars1.githubusercontent.com
151.101.184.133 assets-cdn.github.com
185.199.108.153 documentcloud.github.com
185.199.108.153 help.github.com
18.204.240.114 status.github.com
```
## 加快访问github的方法
1. VPN
	1. 购买vpn，作为学生党就算了吧
	2. 使用一些免费的插件，这种就得自个搜（提醒：谷歌商店一大批免费的，哈哈哈）
2. hosts
	1. 记事本打开C:\Windows\System32\drivers\etc 路径下的hosts文件（映射文件）
	2. 找到上面推荐的解析网站  查询出自个机子适用的dns解析地址（也可以使用我整理好的）
	3. 保存退出（不能保存的请自行百度）
	4. win+r 输入ipconfig /flushdns 刷新dns缓存