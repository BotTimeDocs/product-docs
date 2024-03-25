# FAQ1：安装、激活&登录

<br><br>

## 一、安装、激活&登录

<br>

### Q：安装编辑器或机器人的硬件和软件要求是什么？

<font color=5a6877> 

【解决方法A1_00001】

在安装编辑器或机器人之前，建议您先查看[硬件和软件要求](https://academy.encoo.com/zh-cn/wiki/Studio/quickStart/HarewareAndSoftwareRequirements.md)。为了避免安装失败，建议安装时：
* 关闭杀毒软件
* 使用管理员权限安装

 </font><br><br>
 ---
 <br>



## 二、插件/扩展

### Q：安装扩展时已经关闭所有浏览器窗口，但仍提示关闭浏览器

扩展更新提示，“检测到浏览器插件版本与编辑器不一致，请更新至一致。为完成此更新，请关闭一下所有浏览器后点击确定”。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/2-1.png"/>


<font color=5a6877> 

<br>
<br>

**【解决方法A2_00001】**:

出现该提示时可打开“任务管理器”找到提示的浏览器进程，选中后点击“结束任务”之后重新安装浏览器扩展即可。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/2-2.png"/>

 </font><br><br>
 ---
 <br>

### Q：Chrome 录制失败，无法与 Chrome 扩展通信？
<font color=5a6877> 


**【解决方法A2_00002】**:若出现无法与浏览器扩展通讯的提示，可按照如下步骤排查：

1. 检查 chrome 浏览器扩展，是否安装了 chrome 扩展并且启用，如果未安装“云扩录制器”扩展，需要 通过 Studio 进行自动安装。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/3-1.png"/>



2. 当打开 chrome 后，检查“任务管理器”中是否存在 EncooNativeMessageHost.exe 进程：，该进程是 RPA 与 chrome 浏览器的通信进程，如果不存在，则检查(1)。


**<说明>**
* 如果 EncooNativeMessageHost.exe 进程未启动，需暂时关闭杀毒软件的防护功能，然后 通过 Studio 进行自动安装。
* 如果 EncooNativeMessageHost.exe 进程未启动且已经关闭杀毒软件并安装了扩展，需暂时关闭杀毒软件的防护功能并删除“C:\Users\当前用户\AppData\Local\Encoo\messagehost”文件夹，然后再次通过 Studio 进行安装扩展。
* 如果杀毒软件暂时无法关闭，需要公司超级管理员授权才可关闭时，请用可修改注册表的用户登录，手动修改注册表，手动安装 Chrome 扩展。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/3-2.png"/>


 </font><br><br>
---
<br>
