# Error2：元素定位/识别

 <br>
 
#### Q：使用图像识别定位的元素不支持通过设置控件的方式点击。

<font color=5a6877>
<br>

**【解决办法--AA0001】**：图像识别方式定位元素的，点击方式选择模拟鼠标。

</font>
<br><br>
---
<br>

#### Q：定位元素超时

<font color=5a6877>
<br>

**【解决办法--AA0002】**：定位元素超时可能存在一下几个原因，请注意排查确认
1. 选择器是否能验证到对应的元素？不会请先学习了解选择器
2. 如果以上都没问题，可能是网络加载慢问题，请加长匹配超时的时间。
3. 是否安装了对应的浏览器插件或其它扩展插件并启用？（安装过程关掉杀毒软件）

</font>
<br><br>
---
<br>

#### Q：打开浏览器失败。the operation has timed out

<font color=5a6877>
<br>

**【解决办法--AA0003】**：一般情况下 ，首先请确认是否安装了对应的浏览器插件并启用 ，具体参考链接[Chrome 扩展](https://academy.encoo.com/wiki/Robot/Settings/extensions/ChromeExtension.md)
(若排除以上情况之后，可具体查看下方“打开浏览器失败”的异常排错思路办法)

</font>
<br><br>
---
<br>

#### Q：[错误]设置剪贴板文本失败。详细错误信息：所请求的剪贴板操作失败。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0004.png"/>


<font color=5a6877>
<br>

【原因分析】：

剪贴板调用和实时的运行环境有关，实现上是和命令行一致的。
* 原因1：当剪贴板被占用，或者内存不足时就会失败；
* 原因2：是因为远程(如向日葵)导致共享粘贴板 导致的


<br>

**【解决办法-AA0004】**：为避免出现这个错误可以管理PC内存，检查剪贴板占用，组件前增加延迟、重试或trycath之后选择失败后继续，或者使用其他组件来实现，比如发送快捷键。
补充：( 如果是本身电脑崩溃  你设置粘贴板加重试也没用  它还是粘贴不了 ,一般失败后继续调成1次就足够了)。失败后继续设置图示如下：
<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0004_20220803.png"/>


<br>
</font>
<br><br>
---
<br>


#### Q：用户回调引发异常
* 请检查异常堆栈和内部异常，以确定失败的回调。回调异常的root cause，或者“使用模拟键盘组件会导致流程随机中断，并且可能会伴随“句柄无效”日志”

<font color=5a6877>
<br>

**【解决办法--AA0005】**：淘宝上买 幽灵键鼠 硬件,然后用[模拟键盘合集](https://marketplace.encoo.com/?entry_url=https%3A%2F%2Fwww.encoo.com%2F#/activity/detail?lang=zh-cn&packageId=Automation.KeyboardActivity)里的那个组件 

</font>
<br><br>
---
<br>


#### Q：句柄无效

<font color=5a6877>
<br>

**【解决办法--AA0006】**：同解决办法-AA0005

</font>
<br><br>
---
<br>


#### Q：云扩录制器奔溃了

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0007.jpg"/>


<font color=5a6877>
【原因分析】：环境权限问题导致，偶发异常
<br>

**【解决办法--AA0007】**：

设置对应客户端执行项目的权限为管理员权限执行

（1）机器人界面如何设置管理员权限执行？

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0007-1.png"/>


<br>

（2）编辑器设置界面如何设置管理员权限执行？
* 右键选择项目之后 ，选择设置项目里面 设置对应的权限 

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0007_1.jpg"/>


</font>
<br><br>
---
<br>

#### Q：不能根据选择器获取窗体

<font color=5a6877>

【原因分析】
可能1、可能iframe的问题，谷歌会将这种弹框拦截，视觉上展示了，但是自动化取不到。
可能2、应该是卡在第一层窗体了


<br>

**【解决办法-AA0008】**：
* 第一步、将这个窗口设置成不拦截，后面可以点击到了

> 修改弹窗拦截需进入浏览器中设置的“启动弹窗组织程序”中添加例外：

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202005250001.png"/>

* 第二步、若第一步中可能1排查不存在则验证下元素，进一步排查卡在第一层窗体的哪里 

> 进入选择器查看元素类型，如元素为非浏览器类型（如UIA3）则说明录制元素时未安装或启用浏览器扩展，安装扩展后重新录制即可（录制的元素类型应与浏览器一致，如Chrome）。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202005260001.png"/>

</font>
<br><br>
---
<br>

#### Q：Bitblt调用失败Error:6

<font color=5a6877>
【原因分析】
- 可能1. 运行时，可能系统进入锁屏状态了
- 可能2. 运行时，窗口最小化就会出现这个问题

<br>

**【解决办法--AA0009】**：如果是企业版机器人的话，自带了rdp会话保持功能，如果是远程的话勾选下就好了。

</font>
<br><br>
---
<br>



#### Q：打开浏览器失败

<font color=5a6877>
<br>

**【解决办法--AA0010】**：一般情况下 ，首先请确认是否安装了对应的浏览器插件并启用 ，具体参考链接：[Chrome 扩展](https://academy.encoo.com/wiki/Studio/Extensions/ChromeExtension.md)

</font>
<br><br>
---
<br>

#### Q：手机自动化，Poco Service服务启动异常

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0011.png"/>


<font color=5a6877>
<br>

**【解决办法--AA0011】**：如果用过旧版本的服务端?在“设置”--“应用”里面找到pocoservice的两个软件、Yosemite、Applistmanager软件都卸载删除，重启服务端，再重新连接，其中pocoservice有两个应用，在设置-应用中找到都删载掉。

</font>
<br><br>
---
<br>


#### Q：手机自动化时，提示“请确保移动设备管理器已打开，已有设备连接”

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0012.png"/>

<font color=5a6877>
<br>

**【解决办法--AA0012】**：
1. 确认编辑器菜单栏中”工具 > 移动设备管理器“ 是否已打开。
2. 如果已打开仍未解决，重启移动端服务管理器。

* 移动端服务包无法打开：Failed to execute script EncooAndroidAutomation

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0012-1.png"/>


1. 确认该服务包的版本是否最新，如果非最新，需要重新下载最新版本的服务包。
2. 确认该计算机网络是否正常，如果没有网络则无法获取到网络地址无法打开该应用。

</font>
<br><br>
---
<br>

### Q：IE浏览器 弹窗提示 “停止运行此脚本”

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0013_1.png"/>



<font color=5a6877>
<br>

**【解决办法-AA0013】**：

修改注册表 ，如图所示：创建的类型和上面发的操作里不一样，操作中是DWORD(32位)

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0013_2.png"/>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0013_3.png"/>


</font>
<br><br>
---
<br>

#### Q：浏览器提示“一个或多个ActiveX控件无法显示”如何解决 ？ie浏览器设置后，直接打开使用不出现异常提示弹窗，通过机器人执行就提示这个异常弹窗

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0014.png"/>

<br>


<font color=5a6877>
<br>

**【解决办法--AA0014】**：这个是手动打开不会出现，机器人和编辑器运行都会出现，需要设置：
https://www.iefans.net/a/v760321.html

</font>
<br><br>
---
<br> 

#### Q：(幽灵键鼠)第三方组件会报这个异常"[错误]设备无效"
客户电脑没有接键盘的情况下，我使用DDInput程序和键盘模拟(幽灵键鼠)第三方组件，都无法输入密码，还有其它办法吗？使用键盘模拟

<br>


<font color=5a6877>
<br>

**【解决办法--AA0015】**：使用“键盘模拟”组件 

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0015.png"/>

</font>
<br><br>
---
<br> 

#### Q：[错误]推送文件到手机失败。详细错误信息：指令类型不存在。
推送文件到手机，服务管理器里面这么显示的

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0016.png"/>


<br>


<font color=5a6877>
<br>

**【解决办法--AA0016】**：确认服务包版本同开发版本是否一直 ，不一致的话更换安卓服务包。 



</font>
<br><br>
---
<br> 

#### Q：人工操作网页文本框中输入Enter会出现一个文件上传弹窗，但rpa执行却不会弹出是什么原因。


<br>


<font color=5a6877>
<br>

**【解决办法--AA0017】**：个别网址会出现该情况，原因是编辑器/机器人设置了管理员权限，启动编辑器/机器人时不以管理员权限运行即可。 



</font>
<br><br>
---
<br> 

#### Q：录制网页元素过程中，正常的web元素会被强制识别为UIA3元素，手动切换录制技术也没用。

<br>


<font color=5a6877>
<br>

**【解决办法--AA0018】**：应该是被其他奇怪的Chrome进程干扰导致的，关闭所有Chrome进程后重新打开网页录制即可恢复。 



</font>
<br><br>
---
<br> 