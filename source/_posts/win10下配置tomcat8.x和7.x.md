---
title: win10配置tomcat8.x和7.x
date: 2021-02-15 21:30:37
categories: 技术
tags: win10
---

### 配置tomcat8.x和7.x

#### 配置tomcat7.x

1. 下载并解压apache-tomcat-7.x和apache-tomcat-8.x到文件目录D:\Program Files\Tomcat

2. 配置环境变量

   <!--more-->

   ![image-20210215135022746](https://gitee.com/LYmystery/PicGo/raw/master/image/20210215135030.png)

3. 进入D:\Program Files\Tomcat\apache-tomcat-7.0.68\conf目录，修改server.xml
   1. <Server port="8006" shutdown="SHUTDOWN">修改这个port=”8006”，原来默认的为：8005，使得它的关闭端口和另一个关闭端口不发生冲突。
   2. <Connector port="8081" maxHttpHeaderSize="8192"
              maxThreads="150" minSpareThreads="25" maxSpareThreads="75"
              enableLookups="false" redirectPort="8443" acceptCount="100"
              connectionTimeout="20000" disableUploadTimeout="true" />修改port=”8081”，原来默认的为“8080”，使得它的连接端口和另一个不冲突。
   3. <Connector port="8009" protocol="AJP/1.3" redirectPort="8443" />
      修改这个port=”8010”，原来默认的为：8009，AJP 1.3 Connector定义的地方。

4. 进入D:\Program Files\Tomcat\apache-tomcat-7.0.68\bin修改startup.bat和catalina.bat文件内容，把两个文件所有CATALINA_HOME替换为CATALINA_HOME7。（快捷键Ctrl+H）

5. 启动Tomcat，双击startup.bat，浏览器输入http://localhost:8081 

#### 配置tomcat8.x

1. 由于以tomcat8.x为基准，所以不修改server.xml文件，默认即可
2. 直接修改startup.bat和catalina.bat文件内容，把两个文件所有CATALINA_HOME替换为CATALINA_HOME8。
3. 启动Tomcat，双击startup.bat，浏览器输入http://localhost:8080

#### 后续（tomcat日志乱码问题）

问题原因：

在使用bat文件启动Tomcat时，Tomcat目录下的logs文件夹会生成相应的日志文件，发现旧版本生成的日志文件编码是GBK，而Windows控制台的编码也是GBK，所以不会乱码。而新版本生成的日志文件编码是UTF-8，所以就造成了中文乱码问题

解决：

进入 /conf/logging.properties，这个文件就是tomcat的日志配置文件，通过使用BCompare对新老版本的配置文件进行对比，发现tomcat在新版的日志配置文件中加了指定编码为UTF-8的配置。这就是乱码的根源了。（1）将配置UTF-8那一行配置删除（这样应该就是采用操作系统默认编码，Windows下即为GBK）（2）将UTF-8改为GBK

![image-20210215141038172](https://gitee.com/LYmystery/PicGo/raw/master/image/20210215141039.png)