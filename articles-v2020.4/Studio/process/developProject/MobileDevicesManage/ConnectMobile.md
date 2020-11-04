
# 连接手机
在开发手机客户端软件的时候，通常会使用模拟器和真机两种方式来对APP进行调试，在这里两种方法都会介绍，实际操作过程中，可以根据自己需求来进行选择。

## **Android**

#### **方式一：Android模拟器**

**安卓模拟器**是可以在个人计算机运行并模拟安卓手机系统的模拟器，并能安装、使用、卸载安卓应用的软件，利用安卓模拟器，用户即使没有手机硬件设备，也可以在模拟器中使用移动应用程序。

1. 目前测试或者使用APP的模拟器有很多种，比如MuMu、逍遥、夜神模拟器等，根据自己需求在PC端下载并安装安卓模拟器。

![安卓模拟器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/androidmonitor20201104.png)

2. 与手机类似，需要打开模拟器的 “**开发者选项-允许USB调试** ”。

![开发者选项](https://docimages.blob.core.chinacloudapi.cn/images/Studio/developeroption20201104.png)

> **说明：**
>
> 主流模拟器，可参考下表：

| **序号** | **模拟器名称** | **ADB连接代码**             |
| -------- | -------------- | --------------------------- |
| 1        | 网易mumu       | adb connect 127.0.0.1:7555  |
| 2        | 夜神           | adb connect 127.0.0.1:62001 |
| 3        | 逍遥           | adb connect 127.0.0.1:21503 |
| 4        | iTools         | adb connect 127.0.0.1:54001 |
| 5        | 天天           | adb connect 127.0.0.1:6555  |
| 6        | 海马玩         | adb connect 127.0.0.1:26744 |
| 7        | BlueStacks     | adb connect 127.0.0.1:5555  |

3. <a href="#环境变量">将adb添加到环境变量</a>


4、在PC端的**命令行提示符**界面中，通过模拟器对应的ADB连接代码连接Android终端设备与PC端。

![命令行提示符](https://docimages.blob.core.chinacloudapi.cn/images/Studio/cmd20201104.png)

#### **方式二：Android真机USB连接**

1. 开启开发者模式

每个手机开启开发者模式的方式可能存在差异，如果不知道如何开启自己手机的开发者模式，可以在百度搜索"xxx型号手机如何开启开发者模式"。

> **说明：**
>
> - 在开启开发者模式之后，需要将**开发者选项**中的**USB调试**勾选上。
> - 部分手机需要打开”**允许模拟位置**”、”**允许通过USB安装应用**”。

2. 连接电脑

在连接电脑时，可能需要安装手机的

[驱动程序]: https://product.pconline.com.cn/itbk/sjtx/sjwt/1802/10849872.html

，这样电脑才可以识别打开手机。

3. 连接测试

a. <a name="环境变量">将adb添加到环境变量</a>

> **说明：**
>
> ADB 是Google官方提供的Android调试工具。

​	创建环境变量并添加至Path中

![环境变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/environment20201104.png)

> **说明：**
>
> "D:\workspace\Encoo\Encoo.Android.Automation\airtest\core\android\static\adb\windows"这个路径是我自己存放SDK的文件夹，可以根据自己的实际情况替换。

b. 检查设备是否连接

step1：打开移动端服务包**Encoo.Android.Automation**文件夹。

step2：在服务安装路径"**:\Encoo.Android.Automation**"下，按住shift+鼠标右键打开命令行终端。

![shell窗口](https://docimages.blob.core.chinacloudapi.cn/images/Studio/shellwindow20201104.png)

step3：在终端中输入adb命令，连接成功示例如下:

![连接成功示例](https://docimages.blob.core.chinacloudapi.cn/images/Studio/connectsucess20201104.png)

```shell
>adb.exe devices

List of devices attached

0ddc4c2d(手机的设备号) device
```

> **说明：**
>
> 如果未能连接成功，如下几点可参考：
>
> - 若提示“**adb不是内部或外部命令**”，请检查是否配置了adb的系统环境变量，可参考<a href="#环境变量">**将adb添加到环境变量**</a>。
> - 如果看不到 **设备号 device** 这一行，需要检查电脑上是否已经安装了该款手机的对应官方驱动软件 ，如果尚未安装驱动则检测不到手机，请自行查阅手机品牌官网，下载官方驱动进行安装。
> - 建议尽量使用机箱背面的USB接口，主机正面的USB接口可能稳定性较差。
> - 手机上需要将 开发者选项 开启，并开启 USB调试 选项，并且在接入电脑时，选择 允许该PC对设备进行调试，否则手机状态为**unauthorized**是无法连接的。
> - 需要确认电脑上所有手机助手类型的软件均已关闭，且adb进程都已完全退出（大部分手机助手都需要手动在任务管理器里终止进程）。

## **IOS**

Xcode 是运行在操作系统Mac OS X上的集成开发工具（IDE）,自带各个型号的iphone/ipad/iwatch itv的模拟器，该模拟器用于开发调试，并不能安装App Store上的App。

1. 下载开发调试工具xcode 11.1版本。

   下载链接：https://developer.apple.com/download/more

![安装Xcode](https://docimages.blob.core.chinacloudapi.cn/images/Studio/installxcode20201104.png)

> **说明：**
>
> 若手机系统版本为iOS13.0以上，需要将手机所对应版本的调试包解压后的文件放入/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/DeviceSupport 路径内，并重启Xcode。

1. 安装依赖

在PC终端中进行如下安装操作：

a. 安装brew

brew 是MacOS上的包管理工具，可以简化 macOS 和 Linux 操作系统上软件的安装。

step1：输入安装命令：

```
 /usr/bin/ruby -e "$(curl -fsSL https://hellogithub.cn-bj.ufileos.com/file/brew_install.sh)"
```

戓

```
/usr/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)" 
```

step2：验证是否安装成功。

```
brew --version
```

b. **brew install usbmuxd**

c. **brew install libimobiledevice**

d. **brew install ideviceinstaller** 

3. 获取真机UDID

UDID（Unique Device Identifier ）是由字母和数字组成的 40 个字符串的序号，用来区别每一个唯一的 iOS 设备，包括 iPhones, iPads, 以及 iPod Touches。

在Xcode工具中， 选择**Window - Devices**里查看设备的identifier，复制粘贴，联系开发人员（云扩的开发人员）进行配置可调试证书。

![获取真机UDID](https://docimages.blob.core.chinacloudapi.cn/images/Studio/getudid20201104.png)

> **说明：**
>
> Xcode自带模拟器界面如下图所示。

![iOS模拟器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/iosmonitor20201104.png)

4. 将配置完的证书下载至Xcode工具中

​      a. 打开Xcode工具

![xcode图标](https://docimages.blob.core.chinacloudapi.cn/images/Studio/xcodeicon20201104.png)

​      b. 打开“**Xcode首选项 > Accounts**”，点击界面左下角的“+”，输入Apple ID中的账号（开发者）和密码后保存。

![Xcode账号配置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/xcodeaccount20201104.png)

c. 选择已配置的证书后，单击“**Download Manual Profiles**”下载。

![下载证书](https://docimages.blob.core.chinacloudapi.cn/images/Studio/downloadprofiles20201104.png)
