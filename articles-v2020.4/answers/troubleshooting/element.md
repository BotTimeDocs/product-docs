
### 元素定位/(界面&手机)自动化

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1|元素不支持通过设置控件的方式点击|点击|AA0001
2|定位元素超时|点击|AA0002
3|打开浏览器失败。the operation has timed out|浏览器|AA0003
4|所请求的剪贴板操作失败。|剪贴板、复制粘贴|AA0004
5|用户回调引发异常|网银登录界面|AA0005
6|句柄无效|网银登录界面|AA0006
7|云扩录制器奔溃了|私有化环境、权限问题|AA0007
8|不能根据选择器获取窗体|指定元素|AA0008
9|Bitbit调用失败Error:6|截屏、远程桌面|AA0009
10|打开浏览器失败|浏览器|AA0010
11|Poco Service服务启动异常|手机自动化|AA0011

### 二、具体解决办法

#### 【报错异常】使用图像识别定位的元素不支持通过设置控件的方式点击。

<font color=5a6877>
</br>**【解决办法-AA0001】**：图像识别方式定位元素的，点击方式选择模拟鼠标。

</font>
</br></br>
---
</br>

#### 【报错异常】定位元素超时

<font color=5a6877>
</br>**【解决办法-AA0002】**：定位元素超时可能存在一下几个原因，请注意排查确认
1. 选择器是否能验证到对应的元素？不会请先学习了解选择器
2. 如果以上都没问题，可能是网络加载慢问题，请加长匹配超时的时间。
3. 是否安装了对应的浏览器插件或其它扩展插件并启用？（安装过程关掉杀毒软件）

</font>
</br></br>
---
</br>

#### 【报错异常】打开浏览器失败。the operation has timed out

<font color=5a6877>
</br>**【解决办法-AA0003】**：一般情况下 ，首先请确认是否安装了对应的浏览器插件并启用 ，具体参考链接[Chrome 扩展](https://academy.encoo.com/wiki/Robot/Settings/extensions/ChromeExtension.md?uuid=f63640f7-3a81-46b9-ae53-2ff15e2bc1b8)
(若排除以上情况之后，可具体查看下方“打开浏览器失败”的异常排错思路办法)

</font>
</br></br>
---
</br>

#### 【报错异常】所请求的剪贴板操作失败。

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0004.png)

</br>【原因分析】：剪贴板调用和实时的运行环境有关，实现上是和命令行一致的。当剪贴板被占用，或者内存不足时就会失败。

<font color=5a6877>
</br>**【解决办法-AA0004】**：为避免出现这个错误可以管理PC内存，检查剪贴板占用，组件前增加延迟、重试或trycath之后选择失败后继续，或者使用其他组件来实现，比如发送快捷键
</font>
</br></br>
---
</br>


#### 【报错异常】用户回调引发异常
* 请检查异常堆栈和内部异常，以确定失败的回调。回调异常的root cause，或者“使用模拟键盘组件会导致流程随机中断，并且可能会伴随“句柄无效”日志”

<font color=5a6877>
</br>**【解决办法-AA0005】**：淘宝上买 幽灵键鼠 硬件,然后用[模拟键盘合集](https://marketplace.encoo.com/?entry_url=https%3A%2F%2Fwww.encoo.com%2F#/activity/detail?lang=zh-cn&packageId=Automation.KeyboardActivity)里的那个组件 

</font>
</br></br>
---
</br>


#### 【报错异常】句柄无效

<font color=5a6877>
</br>**【解决办法-AA0006】**：同解决办法-AA0005

</font>
</br></br>
---
</br>


#### 【报错异常】云扩录制器奔溃了

![](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0007.jpg)

<font color=5a6877>
【原因分析】：环境权限问题导致，偶发异常
</br>**【解决办法-AA0007】**：管理员权限执行

![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0007-1.png)

</font>
</br></br>
---
</br>

#### 【报错异常】不能根据选择器获取窗体

<font color=5a6877>
【原因分析】
可能1、可能iframe的问题，谷歌会将这种弹框拦截，视觉上展示了，但是自动化取不到。
可能2、应该是卡在第一层窗体了
</br>**【解决办法-AA0008】**：
* 第一步、将这个窗口设置成不拦截，后面可以点击到了
* 第二步、若第一步中可能1排查不存在则验证下元素，进一步排查卡在第一层窗体的哪里 

</font>
</br></br>
---
</br>

#### 【报错异常】Bitblt调用失败Error:6

<font color=5a6877>
【原因分析】
- 可能1. 运行时，可能系统进入锁屏状态了
- 可能2. 运行时，窗口最小化就会出现这个问题

</br>**【解决办法-AA0009】**：如果是企业版机器人的话，自带了rdp会话保持功能，如果是远程的话勾选下就好了。

</font>
</br></br>
---
</br>



#### 【报错异常】打开浏览器失败

<font color=5a6877>
</br>**【解决办法-AA0010】**：一般情况下 ，首先请确认是否安装了对应的浏览器插件并启用 ，具体参考链接：[Chrome 扩展]()

</font>
</br></br>
---
</br>

#### 【报错异常】手机自动化，Poco Service服务启动异常

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0011.png)

<font color=5a6877>
</br>**【解决办法-AA0011】**：如果用过旧版本的服务端?在“设置”--“应用”里面找到pocoservice的两个软件、Yosemite、Applistmanager软件都卸载删除，重启服务端，再重新连接，其中pocoservice有两个应用，在设置-应用中找到都删载掉。

</font>
</br></br>
---
</br>


#### 【报错异常】手机自动化，请确保移动设备管理器已打开，已有设备连接

![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0012.png)
<font color=5a6877>
</br>**【解决办法-AA0012】**：
1. 确认编辑器菜单栏中”工具 > 移动设备管理器“ 是否已打开。
2. 如果已打开仍未解决，重启移动端服务管理器。

* 移动端服务包无法打开：Failed to execute script EncooAndroidAutomation

![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0012-1.png)

1. 确认该服务包的版本是否最新，如果非最新，需要重新下载最新版本的服务包。
2. 确认该计算机网络是否正常，如果没有网络则无法获取到网络地址无法打开该应用。

</font>
</br></br>
---
</br>
