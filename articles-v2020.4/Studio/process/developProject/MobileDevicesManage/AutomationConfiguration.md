# 步骤 3：自动化服务配置

**自动化服务配置** 主要是在 PC 端配置已下载的移动端服务包与移动端手机设备的连接。当移动端服务包与移动端手机设备连接成功后，移动端服务包（或 移动服务管理器）界面上，可记录服务端地址及端口号，便于编辑器中的“移动设备管理器”连接使用。
## Android

### 连接服务

1. 打开已下载的移动端服务包 **Encoo.Android.Automation.zip** 的解压完成的文件夹。

2. 在解压完成的文件夹中，双击 **Encoo.Android.Automation.exe** 应用程序。

3. 在弹出的 **云扩 Android 服务管理器** 窗口中输入自定义端口号，单击 **连接服务**。

    > **说明：**
    >
    > 自定义的端口号，建议输入 8080~65535 之间的任意数值，但如果连接的模拟器有默认端口，请与之区分。

    ![Android 连接服务](https://docimages.blob.core.chinacloudapi.cn/images/Studio/androidservice20210831.png)

4. 服务连接成功，如下图所示。

    ![服务连接成功](https://docimages.blob.core.chinacloudapi.cn/images/Studio/serverconnectsucess20210831.png)

### 安装 APP 应用（首次）

在解压完成的文件夹下的 **apk** 文件夹中，有以下三个手机应用安装包。根据需要选择对应的 apk 文件, 安装至连接的手机中。

![APP 应用](https://docimages.blob.core.chinacloudapi.cn/images/Studio/encoosmscode20210831.png)

> **说明：**
>
>- “pocoservice-debug”和“Yosemite”由系统默认自主安装，用户无需手动安装。
>- “云扩手机验证码监听器”为配合“获取短信验证码”组件使用，用户按需安装。

| **序号** | **安装包**        | **说明**                                               |
| -------- | ----------------- | ------------------------------------------------------ |
| 1        | pocoservice-debug | 用于显示手机页面元素控件信息。                        |
| 2        | Yosemite          | 测试时默认使用的输入法，测试后可手动修改输入法。       |
| 3        | 云扩手机验证码监听器       | 配合 **获取短信验证码** 组件一起使用, 用于获取短信验证码。<br> **说明：** <br>- 此应用支持 Android 6.0 及以上版本。<br>- "读取短信内容" 权限需设置为“允许”。 |

## IOS

### 连接服务

在 **Mac 电脑** 上进行如下操作：

1. 解压已下载的移动端服务包 **Encoo.IOS.Automation.zip**。

    > **说明：**
    >
    > 需要确保解压路径中不可包含中文字符。

2. 在解压完成的文件夹中，双击 **EncooIOSAutomation** 应用程序。
    > **说明：**
    >- 首次运行该应用时，可能需要在 Mac 的 "设置 > 安全性与隐私" 中打开“允许”开关。
    >- 若双击该应用时，显示“文件已损坏”，可参考 [解决办法](https://www.macdo.cn/925.html)。

3. 在弹出的 **云扩 iOS 服务管理器** 窗口中，单击 **连接服务**。

    ![iOS 连接服务](https://docimages.blob.core.chinacloudapi.cn/images/Studio/iosconnect20201104.png)

> **说明：**
> 启动服务后连接手机，可能会遇到的问题，供参考：
>  - 问题 1：xcode-select: error: tool ‘instruments’requires Xcode 或者 IDE 显示连接时会有相关日志状态输出。
>  <br> 解决参考：
 >  <br> - 查看安装 Xcode 的路径（找到 Xcode，直接拖到终端可查看路径）
 >  <br> -  执行命令 sudo xcode-select --switch 终端中显示的 Xcode 的路径/Contents/Developer/
 > - 问题 2：IDE 连接不上手机。
 > <br> 解决参考：需要检查/usr/bin 文件夹下是否已经安装了 python，若有则需要先卸载掉原先的 python 版本。
