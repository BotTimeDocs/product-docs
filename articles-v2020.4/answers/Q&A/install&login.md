## 一、安装、激活&登录

### Q1：安装编辑器或机器人的硬件和软件要求是什么？

<font color=5a6877> 【解决方法A1_00001】
在安装编辑器或机器人之前，建议您先查看[硬件和软件要求](https://academy.encoo.com/zh-cn/wiki/Studio/quickStart/HarewareAndSoftwareRequirements.md?uuid=1bb922bd-c25d-4921-9241-f13ee45d295f)。为了避免安装失败，建议安装时：
* 关闭杀毒软件
* 使用管理员权限安装

 </font></br></br>
 ---
 </br>

### Q2：使用许可证本地激活编辑器/机器人时，报错：“该许可证不能在当前计算机上注册。”

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A1_00001.png)

<font color=5a6877> 【解决方法A1_00002】:
1. 确认是否为云扩商务提供的正确有效的许可证。
2. 如果许可证过期或无效
    * **过期时：**请在云扩控制台的“管理中心 > 许可证管理”中重新申请许可证。
    

    无效时：将许可证复制粘贴至记事本中，确认是否有多余的空格导致，尤其是许可证字符串的开头或结尾处。


 </font></br></br>
---
</br>

### Q3：使用控制台账号登录机器人时，报错：“连接字符串无效”。

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A1_00001-1.png)

<font color=5a6877> 【解决方法A1_00003】:
1. 确认登录界面上的连接字符串是否为控制台首页中的连接字符串。
2. 如果不是控制台首页中的连接字符串，而是“控制台 > 机器人管理” 中连接机器人的字符串，则需重新复制控制台首页中的连接字符串并使用正确的控制台账号登录。
 </font></br></br>
---
</br>

### Q4：机器人控制台激活时，提示：机器人内部异常，请稍后重试

<font color=5a6877> 【解决方法A1_00004】:情况排查：
已知两个情况：
1. 机器人要求使用的是控制台首页连接字符串，填错成了控制台机器人详情的连接字符串
2. 控制台部署不完整，没有启用websocket支持
备注：其它情况需要研发介入

 </font></br></br>
---
</br>

## 二、插件/扩展

### Q1：安装扩展时已经关闭所有浏览器窗口，但仍提示关闭浏览器

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/2-1.png)

<font color=5a6877> 【解决方法A2_00001】:出现该提示时可打开“任务管理器”找到提示的浏览器进程，选中后点击“结束任务”之后重新安装浏览器扩展即可。

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/2-2.png)

 </font></br></br>
 ---
 </br>

### Q2：Chrome 录制失败，无法与 Chrome 扩展通信？
<font color=5a6877> 【解决方法A2_00002】:若出现无法与浏览器扩展通讯的提示，可按照如下步骤排查：
1. 检查 chrome 浏览器扩展，是否安装了 chrome 扩展并且启用，如果未安装“云扩录制器”扩展，需要 通过 Studio 进行自动安装。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/3-1.png)

2. 当打开 chrome 后，检查“任务管理器”中是否存在 EncooNativeMessageHost.exe 进程：，该进程是 RPA 与 chrome 浏览器的通信进程，如果不存在，则检查(1)。

**<说明>**
* 如果 EncooNativeMessageHost.exe 进程未启动，需暂时关闭杀毒软件的防护功能，然后 通过 Studio 进行自动安装。
* 如果 EncooNativeMessageHost.exe 进程未启动且已经关闭杀毒软件并安装了扩展，需暂时关闭杀毒软件的防护功能并删除“C:\Users\当前用户\AppData\Local\Encoo\messagehost”文件夹，然后再次通过 Studio 进行安装扩展。
* 如果杀毒软件暂时无法关闭，需要公司超级管理员授权才可关闭时，请用可修改注册表的用户登录，手动修改注册表，手动安装 Chrome 扩展。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/3-2.png)

 </font></br></br>
---
</br>
