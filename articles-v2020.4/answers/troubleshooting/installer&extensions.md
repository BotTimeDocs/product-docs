# Error1：常见安装激活(扩展)


<br><br>

#### Q：V3控制台许可证激活，只能激活部分，剩余部分无法激活。报“服务器内部异常”

<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/C0004.png"/>

<font color=5a6877>
<br>

**【解决办法-C0004】**：V3升级V4 可解决对应问题，升级请联系商务。

</font>
<br><br>
---
<br> 

#### Q：使用许可证本地激活编辑器/机器人时，报错：“该许可证不能在当前计算机上注册。”

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A1_00001.png"/>


<font color=5a6877> 【解决方法C0005】:
1. 确认是否为云扩商务提供的正确有效的许可证。
2. 如果许可证过期或无效
    * **过期时：**请在云扩控制台的“管理中心 > 许可证管理”中重新申请许可证。
    

    无效时：将许可证复制粘贴至记事本中，确认是否有多余的空格导致，尤其是许可证字符串的开头或结尾处。


 </font><br><br>
---
<br>

#### Q：使用控制台账号登录机器人时，报错：“连接字符串无效”。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A1_00001-1.png"/>

<font color=5a6877> 【解决方法C0006】:
1. 确认登录界面上的连接字符串是否为控制台首页中的连接字符串。
2. 如果不是控制台首页中的连接字符串，而是“控制台 > 机器人管理” 中连接机器人的字符串，则需重新复制控制台首页中的连接字符串并使用正确的控制台账号登录。
 </font><br><br>
---
<br>

#### Q：机器人控制台激活时，提示：机器人内部异常，请稍后重试

<font color=5a6877> 【解决方法C0007】:情况排查：
已知两个情况：
1. 机器人要求使用的是控制台首页连接字符串，填错成了控制台机器人详情的连接字符串
2. 控制台部署不完整，没有启用websocket支持
备注：其它情况需要研发介入

 </font><br><br>
---
<br>

#### Q：此应用无法在你的电脑上运行

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-1.png"/>


<font color=5a6877>
<br>

**【解决办法-I0001】**
* Step1、确认一下【计算机配置】—【Windows设置】—【安全设置】—【本地策略】—【安全选项】 已经启用了用户账户控制：以管理员批准模式运行所有管理员…… 

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-3.png"/>

<br>

* Step2、如果上一步还是不行，那安装包可能被串改了，重新下载一个安装包吧，注意安装的时候 关闭一下 杀毒软

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-4.png"/>


</font><br><br>
---
<br>

#### Q：未将对象引用设置到对象的实例
* 编辑器安装时，显示发生了以下错误，错误信息：未将对象引用设置到对象的实例

<br>

<font color=5a6877>

**【解决办法-I0002】**

编辑器安装失败确认排查步骤如下 ：
- Step1：检查杀毒软件是否正在运行，关闭杀毒软件(如，360 软件)后重新安装。
- Step2：可在控制面板中，检查是否安装“.net 中文语言包”，如果安装了，可以卸载后再尝试，如果没有安装，可检查日志。卸载后若没安装.net去下载安装一下对应的的英文版安装包，具体选项示例如下方所示

</font><br><br>
---
<br>


#### Q：这计算机中已经安装了.NET Framework 4.6.2(简体中文)或版本更高的更新

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0003.png"/>


<font color=5a6877>
<br>

**【解决办法-I0003】**
* 如果重新安装.NET Framework依然失败提示同样错误信息，那么需要清理注册表
Software\Microsoft\Windows\CurrentVersion\Uninstall\Microsoft .NET Framework 4 Client Profile CHS Language Pack

</font><br><br>
---
<br>

#### Q：Install .Net 4.6.2

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0021.png"/>

<font color=5a6877>
<br>

**【解决办法-I0021】**我们安装包自带.net 4.6.2的，如果系统没有.net 4.6.2，安装我们产品时也会自动安装4.6.2。那其实最终原因还是之前电脑的net坏了，不是版本问题。或者之

</font><br><br>
---
<br>

#### Q：[Installation has failed]There was an error while installing the application.Check the setup log for more information and contact the author

<font color=5a6877>
<br>

**【解决办法-I0004】**编辑器安装失败确认排查步骤如下 ：
* Step1：检查杀毒软件是否正在运行，关闭杀毒软件(如，360 软件)后重新安装。
* Step2：检查当前用户在安装目录的读写权限，如果当前用户在安装路径没有读写权限，则要用管理员账号登录，在安装目录右键，点击属性，点击安全标签，添加目标账户，并添加完全控制权限，最后点击确定，然后退出管理员账号，用目标用户登录进行安装。

</font><br><br>
---
<br>

#### Q：[Installation has failed] Failed to install the .NET Framework,try installing the latest version manually

<font color=5a6877>
<br>

**【解决办法-I0005】**robot运行是基于.net环境的，如果是win7操作系统，则需要手动安装下.net插件，可以通过离线包安装

</font><br><br>
---
<br>

#### Q：Value cannot be null.Parameter name:path1

<font color=5a6877>
<br>

**【解决办法-I0006】**开启杀毒软件导致的，关闭后重新安装就好了
</font><br><br>
---
<br>

#### Q：该许可证不能在当前计算机上注册|本地许可证激活

<font color=5a6877>
<br>

**【解决办法-I0007】**
请联系商务确认是否许可证不对，若不对重新购买或申请许可证
</font><br><br>
---
<br>

#### Q：Java扩展安装失败!

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/E0001.png"/>


<font color=5a6877>
<br>

**【解决办法-E0001】**
- 有网络情况 —— 登录编辑器之后再按照 
- 无网络离线情况 —— 参考手动安装扩展，具体参考链接:(https://academy.encoo.com/wiki/Robot/Settings/extensions/ChromeExtension.md)

</font><br><br>
---
<br>

#### Q：检测到Java应用程序,请更新Java插件

<font color=5a6877>
<br>

**【解决办法-E0002】**
- 第一步 ：更新Java拓展 
- 第二步：若还是不行，继续弹这个提示，禁用默认jab, jre bin目录下有个jabswitch.exe.
cmd 执行 “jabswitch.exe -disable”

</font><br><br>
---
<br>

#### Q：无效许可提示|激活机器人
<br>
* 机器人激活许可证时候，之前可以正常激活，重新卸载激活机器人报"无效许可提示"

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0001.png"/>

<font color=5a6877>
<br>

**【解决办法-R0001】**
* 首先确认电脑系统无重装，且无更换电脑或服务器后确认。
* 然后确认前后使用许可的机器人安装包版本是否一致 。
</font><br><br>
---
<br>

#### Q：尚未安装.Net Framework 4.6.2,原因是：时间戳签名和/或证书无法验证或已损坏 

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0008.png"/>

<font color=5a6877>

【原因分析】
1. 问题描述：不受信任的证书 —— 原因：证书未安装
2. 问题描述：时间戳签名和/或证书无法验证或已损坏 —— 原因：系统版本太老

<br>

**【解决办法-I0008】**

1. 解决方法：MicrosoftRootCertificateAuthority2011.cer 去网上下载此证书点击安装即可

2. 解决方法：安装KB2813430补丁；    
    * [32位系统补丁下载地址（点击下载)](https://www.microsoft.com/zh-CN/download/details.aspx?id=39110)
    * [64位系统补丁下载地址](https://www.microsoft.com/zh-CN/download/details.aspx?id=39115)

补充：[推荐相关阅读-(点击查看)](https://blog.csdn.net/wl_tian_dao_chou_qin/article/details/123002341?ops_request_misc=&request_id=&biz_id=102&utm_term=%E6%97%B6%E9%97%B4%E6%88%B3%E7%AD%BE%E5%90%8D%E5%92%8C%E6%88%96%E8%AF%81%E4%B9%A6&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-123002341.142^v13^pc_search_result_control_group,157^v14^new_3&spm=1018.2226.3001.4187)


</font >

</font><br><br>
---
<br>

#### Q：应用程序发送异常 未知的软件异常（0xe0434352），位置为0x76f7c5af。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/0xe0434352.png"/>

<br>

<font color=5a6877>

**【解决办法-I0009】**

插件安装包崩溃了。几种可能性：
* 一个是权限不够，试试看管理员运行；
* 二是文件损坏，缺东西之类的，可以重新下载一个安装试试；
* 三是系统里有什么管理阻碍运行，比如杀毒工具或者系统管理的工具之类

</font >

</font><br><br>
---
<br>

### Q：[Installation has failed ]
There was an error while installing the application.Check the setup log for more information and contact the author.

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I00010.png"/>


<br>

<font color=5a6877>

**【解决办法-I0018】** .net环境坏掉了 重装一下

</font >

</font><br><br>
---
<br>

#### Q:弹窗错误提示“应用程序无法启动，因为应用程序的并行配置不正确。有关详细信息，请参阅应用程序事件日志，或使用命令行sxstrace.exe 工具”

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I00011.png"/>

<br>

<font color=5a6877>

原因分析：由于系统文件损坏或 Visual C++ 可再发行包损坏，可能会发生此错误。

<br>

**【解决办法-I0019】**：

* **方法一：**

请从下面给出的链接下载并安装 Microsoft Visual C++ 2013 Redistributable Package 并检查它是否有帮助：

适用于 Visual Studio 2013 的 Visual C++ 可再发行包

http://www.microsoft.com/en-in/download/details.aspx?id=40784

* **方法二：**

我建议你运行系统文件检查器。系统文件检查器 (SFC) 扫描已完成以检查是否有任何损坏的系统文件可能导致此问题。请按照以下给定步骤操作：

按 Windows 键 + X，选择命令提示符（管理员）以调出提升的命令提示符。
在命令提示符下键入 sfc/scannow 并按 Enter。
重新启动计算机。
如果在之前的状态下没有发现损坏的系统文件，那么我建议您尝试以下步骤：

按 Windows 键 + X 并选择“命令提示符管理员”打开命令提示符。
在命令提示符下，键入以下命令并在每个命令后按 Enter：
```
DISM.exe /在线 /Cleanup-image /Scanhealth

DISM.exe /Online /Cleanup-image /Restorehealth
```
关闭命令提示符并重新启动 PC 并检查它是否正常工作。

参考链接：[《The application has failed to start because the side by side configuration is incorrect Windows 10》](https://answers.microsoft.com/en-us/windows/forum/all/the-application-has-failed-to-start-because-the/5c6a015e-4162-491d-b7d9-f3b13612e304)
</font>
<br><br>
---
<br> 