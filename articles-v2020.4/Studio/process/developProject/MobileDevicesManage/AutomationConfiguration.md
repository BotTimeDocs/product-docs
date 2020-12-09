# 步骤3：自动化服务配置

## Android

### 连接服务

1. 解压已下载的移动端服务包**Encoo.Android.Automation.zip**。

> **说明：**
>
> 需要确保解压路径中不可包含中文字符。

2. 在解压完成的文件夹中，双击**Encoo.Android.Automation.exe**应用程序。

3. 在弹出的**云扩Android服务管理器**窗口中，单击**连接服务**。

![Android连接服务](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Andriodconnect20201104.png)

4. 服务连接成功，如下图所示。

![服务连接成功](https://docimages.blob.core.chinacloudapi.cn/images/Studio/serverconnectsucess20201104.png)

### 安装APP应用（首次）

在解压完成的文件夹下的 **apk** 文件夹中，有以下三个手机应用安装包，按需使用进行安装。

![APP应用](https://docimages.blob.core.chinacloudapi.cn/images/Studio/app20201104.png)

| **序号** | **安装包**        | **说明**                                               |
| -------- | ----------------- | ------------------------------------------------------ |
| 1        | pocoservice-debug | 用于显示手机页面元素控件信息。                         |
| 2        | SmsObserver       | 配合**获取短信验证码**组件一起使用,用于获取短信验证码。<br>**说明：**<br>- 此应用支持 Android 6.0及以上版本。<br>- "读取短信内容"权限需设置为“允许”。 |
| 3        | Yosemite          | 测试时默认使用的输入法，测试后可手动修改输入法。       |

## IOS

### 连接服务

在 **Mac电脑**上进行如下操作：

1. 解压已下载的移动端服务包**Encoo.IOS.Automation.zip**。

> **说明：**
>
> 需要确保解压路径中不可包含中文字符。

2. 在解压完成的文件夹中，双击**EncooIOSAutomation**应用程序。
>**说明：**
>- 首次运行该应用时，可能需要在 Mac 的"设置 > 安全性与隐私"中打开“允许”开关。
>- 若双击该应用时，显示“文件已损坏”，可参考[解决办法](https://www.macdo.cn/925.html)。

1. 在弹出的**云扩iOS服务管理器**窗口中，单击**连接服务**。

![iOS连接服务](https://docimages.blob.core.chinacloudapi.cn/images/Studio/iosconnect20201104.png)
>**说明：**
>启动服务后连接手机，可能会遇到的问题，供参考：
>  - 问题1：xcode-select: error:tool ‘instruments’requires Xcode或者IDE显示连接时会有相关日志状态输出。
>  解决参考：
 >     - 查看安装Xcode的路径（找到Xcode，直接拖到终端可查看路径）
 >    -  执行命令sudo xcode-select --switch终端中显示的Xcode的路径/Contents/Developer/
 > - 问题2：IDE 连接不上手机。
 >  解决参考：需要检查/usr/bin文件夹下是否已经安装了python，若有则需要先卸载掉原先的python版本。