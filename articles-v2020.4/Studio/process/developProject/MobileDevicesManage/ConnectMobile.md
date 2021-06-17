# 步骤 2：连接手机

在开发手机客户端软件的时候，通常会使用模拟器和真机两种方式来对 APP 进行调试，在这里两种方法都会介绍，实际操作过程中，可以根据自己需求来进行选择。

> **注意：**
>
> 如 PC 端已打开“360 安全助手”等安全软件，请在服务前关闭此类软件。
  
## Android

### 前提条件

PC端在连接Android设备之前需配置ADB环境。**ADB** 是 Google 官方提供的 Android 调试工具，需配置该服务后PC和Android端才能正常连接。

1. 解压已下载的移动端服务包 Encoo.Android.Automation.zip，复制其adb.exe所在的路径。路径格式为：“(**PC 文件路径**)\Encoo.Android.Automation\airtest\core\android\static\adb\windows”，其中括号内内容根据实际情况改变，其余部分不变。

    > **说明：**
    >
    > 需要确保解压路径中不可包含中文字符。

2. 创建 adb 系统环境变量。在PC端操作系统的“高级系统设置 > 高级 > 环境变量”中，为“Path”变量追加赋值。例如：`D:\workspace\Encoo\Encoo.Android.Automation\airtest\core\android\static\adb\windows`。

    ![环境变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/environment20201104.png)

    > **注意：**
    >
    > - 若系统环境变量中已存在其它 ADB 环境变量的配置（如，模拟器），需删除对应 ADB 环境变量的配置。
    > - 若每次更新安卓服务包时，服务路径会发生改变，需重新配置 ADB 环境变量。

3. 验证ADB环境变量是否已配置成功。打开“命令提示符”窗口，输入`adb`命令后回车，显示如下信息，则表示配置成功。

    ![验证ADB环境变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/confirmadb20210617.png)

### 方式一：Android 模拟器

**安卓模拟器** 是可以在个人计算机运行并模拟安卓手机系统的模拟器，并能安装、使用、卸载安卓应用的软件，利用安卓模拟器，用户即使没有手机硬件设备，也可以在模拟器中使用移动应用程序。

1. 目前测试或者使用 APP 的模拟器有很多种，比如 MuMu 、逍遥、夜神模拟器等，根据自己需求在 PC 端下载并安装安卓模拟器。

    ![安卓模拟器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/androidmonitor20201104.png)

2. 与手机类似，需要打开模拟器的 **开发者选项-允许 USB 调试** 。

    ![开发者选项](https://docimages.blob.core.chinacloudapi.cn/images/Studio/developeroption20201104.png)

    > **说明：**
    >
    > 主流模拟器，可参考下表：

    | **序号** | **模拟器名称** | **ADB 连接代码**             |
    | -------- | -------------- | --------------------------- |
    | 1        | 网易 mumu       | adb connect 127.0.0.1: 7555  |
    | 2        | 夜神           | adb connect 127.0.0.1: 62001 |
    | 3        | 逍遥           | adb connect 127.0.0.1: 21503 |
    | 4        | iTools         | adb connect 127.0.0.1: 54001 |
    | 5        | 天天           | adb connect 127.0.0.1: 6555  |
    | 6        | 海马玩         | adb connect 127.0.0.1: 26744 |
    | 7        | BlueStacks     | adb connect 127.0.0.1: 5555  |

3. 在 PC 端的 **命令行提示符** 界面中，通过模拟器对应的 ADB 连接代码连接 Android 终端设备与 PC 端。

    ![命令行提示符](https://docimages.blob.core.chinacloudapi.cn/images/Studio/cmd20201104.png)

### 方式二：Android 真机 USB 连接

目前支持的手机系统版本为 Android 4.4 至 Android 10 ，其中基于 Android 9 和 Android 10 的 MIUI 11 和 MIUI 12 系统除外。

1. Android 真机通过 USB 数据线与 PC 端进行连接。
2. 开启开发者模式

   每个手机开启开发者模式的方式可能存在差异，如果不知道如何开启自己手机的开发者模式，可以在百度搜索 "xxx 型号手机如何开启开发者模式"。

   > **说明：**
   >
   > - 在开启开发者模式之后，需要将 **开发者选项** 中的 **USB 调试** 勾选上。
   > - 部分手机需要打开”**允许模拟位置**”、”**允许通过 USB 安装应用**”。

3. 连接电脑

   在连接电脑时，可能需要安装手机的驱动程序，这样电脑才可以识别打开手机。
   > **说明：**
   > 一般情况下数据线连接 PC 端 USB 接口时，会自动安装手机驱动，除非 PC 端弹出“安装驱动失败”等提示才需手动安装。

4. 连接测试

   在 PC 端的 **命令行提示符** 界面中，输入 `adb devices` 命令，连接成功示例如下:

   ![连接成功示例](https://docimages.blob.core.chinacloudapi.cn/images/Studio/deviceconnect20210129.png)

   > **说明：**
   >
   > 如果未能连接成功，如下几点可参考：
   >
   > - 若提示 **adb 不是内部或外部命令**，请检查是否配置了 adb 的系统环境变量。
   > - 如果看不到 **设备号 device** 这一行，需要检查电脑上是否已经安装了该款手机的对应官方驱动软件 ，如果尚未安装驱动则检测不到手机，请自行查阅手机品牌官网，下载官方驱动进行安装。
   > - 建议尽量使用机箱背面的 USB 接口，主机正面的 USB 接口可能稳定性较差。
   > - 手机上需要将 开发者选项 开启，并开启 USB 调试 选项，并且在接入电脑时，选择 允许该 PC 对设备进行调试，否则手机状态为 **unauthorized** 是无法连接的。
   > - 需要确认电脑上所有手机助手类型的软件均已关闭，且 adb 进程都已完全退出（大部分手机助手都需要手动在任务管理器里终止进程）。

## IOS

Xcode 是运行在操作系统 Mac OS X 上的集成开发工具（IDE）, 自带各个型号的 iphone/ipad/iwatch itv 的模拟器，该模拟器用于开发调试，并不能安装 App Store 上的 App 。

在 **Mac 电脑** 上进行如下操作：
> **说明：**
>
> Mac 电脑与手机连接时：建议手机的 **锁定屏幕**(手机设置-显示与亮度-自动锁定)设置为 **永不**，防止录制或回放过程中手机锁屏导致操作失败。

1. 下载开发调试工具 xcode 11.1 版本。

   下载链接：`https://developer.apple.com/download/more`

    ![安装 Xcode](https://docimages.blob.core.chinacloudapi.cn/images/Studio/installxcode20201104.png)

    > **说明：**
    >
    > - 若手机系统版本为 iOS 13.0 以上（暂不支持 iOS 14.0 及以上系统），需要将手机所对应版本的调试包解压后的文件放入/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/DeviceSupport 路径内，并重启 Xcode。
    > - 各版本调试包下载链接：`https://pan.baidu.com/s/1O9x8-wE0UIsA7GLWdLrMkw`  密码：`refx`

2. 安装依赖

    在 Mac PC 终端中进行如下安装操作：

    a. **安装 brew**

    brew 是 MacOS 上的包管理工具，可以简化 macOS 和 Linux 操作系统上软件的安装。

    step1：输入安装命令：

    ```bash
    /usr/bin/ruby -e "$(curl -fsSL https://hellogithub.cn-bj.ufileos.com/file/brew_install.sh)"
    ```

   或

    ```bash

    /usr/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)" 
    ```

    step2：验证是否安装成功。

    ```bash
    brew --version
    ```

    > **说明：**
    >
    > 在操作过程中，可能会遇到如下问题，供参考：
    >
    > - 问题 1：Homebrew 安装报错 `curl : (7) Failed to connect to raw.githubusercontent.com port 443: Operation`
    > 解决参考：`https://www.jianshu.com/p/dea776e7effb` 或  `https://blog.csdn.net/heroacool/article/details/102844367`
    > - 问题 2：`/usr/bin/zsh：No such file or directory`
    > 解决参考: `brew install zsh
    > https://www.cnblogs.com/mafeng/p/10569559.html`
    > - 问题 3：brew 安装超时，速度慢
    >  解决参考: `https://www.jianshu.com/p/6b486e12454f`

    b. **brew install usbmuxd**
    > **说明：**
    >
    > 在操作过程中，可能会遇到如下问题，供参考：
    >
    > - 问题 1：local 权限问题
    > 解决参考：`https://www.cnblogs.com/tinys-top/p/12299663.html`

    c. **brew install libimobiledevice**

    d. **brew install ideviceinstaller**

3. 获取真机 UDID

    UDID（Unique Device Identifier ）是由字母和数字组成的 40 个字符串的序号，用来区别每一个唯一的 iOS 设备，包括 iPhones, iPads, 以及 iPod Touches。

    在 Xcode 工具中， 选择 **Window - Devices** 里查看设备的 identifier ，复制粘贴，联系开发人员（云扩的开发人员）进行配置可调试证书。

    ![获取真机 UDID](https://docimages.blob.core.chinacloudapi.cn/images/Studio/getudid20201104.png)

    > **说明：**
    >
    > Xcode 自带模拟器界面如下图所示。

    ![iOS 模拟器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/iosmonitor20201104.png)

4. 将配置完的证书下载至 Xcode 工具中

​    a. 打开 Xcode 工具

   ![xcode 图标](https://docimages.blob.core.chinacloudapi.cn/images/Studio/xcodeicon20201104.png)

​    b. 打开 **Xcode 首选项 > Accounts**，点击界面左下角的“+”，输入 Apple ID 中的账号（开发者）和密码后保存。

   ![Xcode 账号配置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/xcodeaccount20201104.png)

   c. 选择已配置的证书后，单击 **Download Manual Profiles** 下载。

   ![下载证书](https://docimages.blob.core.chinacloudapi.cn/images/Studio/downloadprofiles20201104.png)
