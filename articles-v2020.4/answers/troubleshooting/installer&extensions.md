

### 一、编辑器/机器人/插件扩展_安装、激活 （报错索引）

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1| 此应用无法在你的电脑上运行 |编辑器安装|I0001
2| 未将对象引用设置到对象的实例 |编辑器安装|I0002
3| 这计算机中已经安装了.NET </br>Framework </br>4.6.1(简体中文)或版本更高的更新 |编辑器安装|I0003
4| [Installation has failed]</br>There was an error while installing</br> the application.Check</br> the setup log for more information </br>and contact the author |编辑器安装|I0004
5| [Installation has failed]</br> Failed to install</br>the .NET Framework,try installing the</br> latest version manually |编辑器安装|I0005
6| Value cannot be null.</br>Parameter name:path1|编辑器安装 |I0006
7| 该许可证不能在当前计算机上注册|编辑器本地激活 |I0007
8| Java扩展安装失败! |扩展安装|E0001
9| 检测到Java应用程序,</br>请更新Java插件 |扩展安装|E0002
10| 无效许可提示 |激活机器人|R0001
11| 尚未安装.Net Framework 4.6.2,</br>原因是：时间戳签名和/或</br>证书无法验证或已损坏 |编辑器安装|I0008

<br>


### 二、具体解决办法

####【报错异常】此应用无法在你的电脑上运行

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-1.png)

<font color=5a6877>
</br>**【解决办法-I0001】**
* Step1、确认一下【计算机配置】—【Windows设置】—【安全设置】—【本地策略】—【安全选项】 已经启用了用户账户控制：以管理员批准模式运行所有管理员…… 

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-3.png)

</br>

* Step2、如果上一步还是不行，那安装包可能被串改了，重新下载一个安装包吧，注意安装的时候 关闭一下 杀毒软

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-4.png)

</font></br></br>
---
</br>

####【报错异常】未将对象引用设置到对象的实例
* 编辑器安装时，显示发生了以下错误，错误信息：未将对象引用设置到对象的实例

</br>

<font color=5a6877>
**【解决办法-I0002】**编辑器安装失败确认排查步骤如下 ：
- Step1：检查杀毒软件是否正在运行，关闭杀毒软件(如，360 软件)后重新安装。
- Step2：可在控制面板中，检查是否安装“.net 中文语言包”，如果安装了，可以卸载后再尝试，如果没有安装，可检查日志。卸载后若没安装.net去下载安装一下对应的的英文版安装包，具体选项示例如下方所示

</font></br></br>
---
</br>


####【报错异常】这计算机中已经安装了.NET Framework 4.6.1(简体中文)或版本更高的更新

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0003.png)

<font color=5a6877>
</br>**【解决办法-I0003】**
* 如果重新安装.NET Framework依然失败提示同样错误信息，那么需要清理注册表
Software\Microsoft\Windows\CurrentVersion\Uninstall\Microsoft .NET Framework 4 Client Profile CHS Language Pack

</font></br></br>
---
</br>

####【报错异常】[Installation has failed]There was an error while installing the application.Check the setup log for more information and contact the author

<font color=5a6877>
</br>**【解决办法-I0004】**编辑器安装失败确认排查步骤如下 ：
* Step1：检查杀毒软件是否正在运行，关闭杀毒软件(如，360 软件)后重新安装。
* Step2：检查当前用户在安装目录的读写权限，如果当前用户在安装路径没有读写权限，则要用管理员账号登录，在安装目录右键，点击属性，点击安全标签，添加目标账户，并添加完全控制权限，最后点击确定，然后退出管理员账号，用目标用户登录进行安装。

</font></br></br>
---
</br>

####【报错异常】[Installation has failed] Failed to install the .NET Framework,try installing the latest version manually

<font color=5a6877>
</br>**【解决办法-I0005】**robot运行是基于.net环境的，如果是win7操作系统，则需要手动安装下.net插件，可以通过离线包安装

</font></br></br>
---
</br>

####【报错异常】Value cannot be null.Parameter name:path1

<font color=5a6877>
</br>**【解决办法-I0006】**开启杀毒软件导致的，关闭后重新安装就好了
</font></br></br>
---
</br>

####【报错异常】该许可证不能在当前计算机上注册|本地许可证激活

<font color=5a6877>
</br>**【解决办法-I0007】**
请联系商务确认是否许可证不对，若不对重新购买或申请许可证
</font></br></br>
---
</br>

####【报错异常】Java扩展安装失败!

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/E0001.png)

<font color=5a6877>
</br>**【解决办法-E0001】**
- 有网络情况 —— 登录编辑器之后再按照 
- 无网络离线情况 —— 参考手动安装扩展，具体参考链接:(https://academy.encoo.com/wiki/Robot/Settings/extensions/ChromeExtension.md?uuid=f63640f7-3a81-46b9-ae53-2ff15e2bc1b8)

</font></br></br>
---
</br>

####【报错异常】检测到Java应用程序,请更新Java插件

<font color=5a6877>
</br>**【解决办法-E0002】**
- 第一步 ：更新Java拓展 
- 第二步：若还是不行，继续弹这个提示，禁用默认jab, jre bin目录下有个jabswitch.exe.
cmd 执行 “jabswitch.exe -disable”

</font></br></br>
---
</br>

####【报错异常】无效许可提示|激活机器人
</br>
* 机器人激活许可证时候，之前可以正常激活，重新卸载激活机器人报"无效许可提示"

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0001.png)

<font color=5a6877>
</br>**【解决办法-R0001】**
* 首先确认电脑系统无重装，且无更换电脑或服务器后确认。
* 然后确认前后使用许可的机器人安装包版本是否一致 。
</font></br></br>
---
</br>

#### 【报错异常】尚未安装.Net Framework 4.6.2,原因是：时间戳签名和/或证书无法验证或已损坏 

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0008.png)

<font color=5a6877>

【原因分析】
1. 问题描述：不受信任的证书 —— 原因：证书未安装
2. 问题描述：时间戳签名和/或证书无法验证或已损坏 —— 原因：系统版本太老

</br>**【解决办法-I0008】**

1. 解决方法：MicrosoftRootCertificateAuthority2011.cer 去网上下载此证书点击安装即可

2. 解决方法：安装KB2813430补丁；    
    * [32位系统补丁下载地址（点击下载)](https://www.microsoft.com/zh-CN/download/details.aspx?id=39110)
    * [64位系统补丁下载地址](https://www.microsoft.com/zh-CN/download/details.aspx?id=39115)

补充：[推荐相关阅读-(点击查看)](https://blog.csdn.net/wl_tian_dao_chou_qin/article/details/123002341?ops_request_misc=&request_id=&biz_id=102&utm_term=%E6%97%B6%E9%97%B4%E6%88%B3%E7%AD%BE%E5%90%8D%E5%92%8C%E6%88%96%E8%AF%81%E4%B9%A6&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-123002341.142^v13^pc_search_result_control_group,157^v14^new_3&spm=1018.2226.3001.4187)


</font >

</font></br></br>
---
</br>
