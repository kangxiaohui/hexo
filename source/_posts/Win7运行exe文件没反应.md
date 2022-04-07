# Win7运行exe文件没反应

在Win7系统中打开exe可执行文件，只要双击就可以打开，可是有些用户遇到了无法打开的情况，检查exe文件一切都是正常的。很多用户不知该如何处理？那遇到这样的情况我们应该怎么去解决呢？现在小编就和大家说一下Win7运行exe文件没反应的解决方法。

　　**方法如下：**

　　1、新建记事本复制以下内容粘贴到记事本中。

![](https://gitee.com/LYmystery/PicGo/raw/master/img/20210414084039.jpg)

　　2、添加以下内容：Windows Registry Editor Version 5.00

　　［HKEY_CLASSES_ROOT.exe］

　　@=“exefile”

　　“Content Type”=“application/x-msdownload”

　　［HKEY_CLASSES_ROOT.exePersistentHandler］

　　@=“{098f2470-bae0-11cd-b579-08002b30bfeb}”

　　3、然后把记事本保存为“.reg”文件，或修改后缀名为“.reg”，然后双击并导入文件。

![](https://gitee.com/LYmystery/PicGo/raw/master/img/20210414084244.jpg)