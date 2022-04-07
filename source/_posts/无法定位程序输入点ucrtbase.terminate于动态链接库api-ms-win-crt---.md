![无法定位程序输入点ucrtbase.terminate于动态链接库api-ms-win-crt---](https://pic1.zhimg.com/v2-19706ca6f12441a399e2360e9dac907b_1440w.jpg?source=172ae18b)

# 无法定位程序输入点ucrtbase.terminate于动态链接库api-ms-win-crt---

打开软件提示“无法定位程序输入点ucrtbase.terminate于动态链接库api-ms-win-crt-runtime-|1-1-0.dll”的解决方案：

1、按下“WIN+R”打开运行，输入cmd打开命令提示符输入 winver.exe ，按回车。

![img](https://pic2.zhimg.com/v2-d5451cf88b457aac1ab63553b8f17fe1_r.jpg)

2、查看Windows 7系统版本。

![img](https://pic3.zhimg.com/v2-9d151bc5c98cb7c9e519ed61bc045e3e_r.jpg)

3、如果版本为7600，先把系统升级为7601。

[![img](https://zhstatic.zhihu.com/assets/zhihu-components/file-icon/zhimg_answer_editor_file_other.svg)7601.17514.101119-1850_Update_Sp_Wave1-GRMSP1.1_DVD.iso2G·百度网盘](https://pan.baidu.com/link/zhihu/7Vh0zUuYhWiTc0tk81bSJOBHMtelJ2dQQ2FW==)

4、版本升级为 7601后，安装以下两个组件

![img](https://pic3.zhimg.com/v2-78fb8a1f576b8dc23b2786375d107706_r.jpg)

5、安装 net4.6.1

[![img](https://zhstatic.zhihu.com/assets/zhihu-components/file-icon/zhimg_answer_editor_file_other.svg)NDP461-KB3102438-Web.exe1.4M·百度网盘](https://pan.baidu.com/link/zhihu/7dhHzbubh1iULYBD10bWFzZWWCU490dQQYxU==)



6、安装 Visual C++2015

[![img](https://zhstatic.zhihu.com/assets/zhihu-components/file-icon/zhimg_answer_editor_file_other.svg)vc_redist.x64.exe14.6M·百度网盘](https://pan.baidu.com/link/zhihu/7Ah3zRuVh5ikVkFmdUbq1uJUW4bw0USwdpdH==)

7、等这两个系统组件安装完成后重启一下电脑，然后测试软件是否正常运行。



编辑于 2020-06-10