---
title: VSCode过滤文件配置
categories: 技术
date: 2021-02-15 20:39:43
tags: vscode
---

打开vscode，添加文件后，文件列表会出现大量与代码无关的文件，看着很不爽，这时只需要在设置一下即可

打开设置文件夹settings.json

<!--more-->

![img](https://img-blog.csdnimg.cn/20190823185213415.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzODI3NTk1,size_16,color_FFFFFF,t_70)

过滤文件夹方法：          **"\**/文件夹名": true,**  
如：.git是文件夹名

过滤以固定后缀结尾的文件： **"\**/\*.后缀名": true,**  
如：exe是后缀名

**在设置里加入这段代码(可根据个人需要更改)即可**

```json
      "files.exclude": {
        "**/.git": true,
        "**/.svn": true,
        "**/.hg": true,
        "**/CVS": true,
        "**/.DS_Store": true,
        "**/.vscode": true,
        "**/*.exe": true, 
      },
```

至此vscode文件列表就简洁了很多