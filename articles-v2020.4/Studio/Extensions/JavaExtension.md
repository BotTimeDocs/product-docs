# Java 扩展

**Java 扩展** 适用于 Java1.6 及以上应用程序的自动化。

  > **说明：**
  >
  > 对于使用 Java 9+ JRE 打开的应用程序：
  >
  >- 在 Java 9 之前，JRE 会包含 attach 模块，Java 扩展依赖其对 Java 程序进行自动化。
  >- 对于 Java 9+，attach 模块仅包含在 JDK 中，所以对于使用 JRE9+打开的程序，需要手动在 JRE 目录下添加此模块。

## 从编辑器安装

1. **关闭所有 Java 应用，** 点击编辑器左侧工具栏上“工具”图标。
2. 选择“扩展 > Java 扩展”后，将会弹出确认窗口。
3. 点击”确定“后，会以管理员权限启动 Java 扩展安装程序，点击用户账户控制窗口上的“是”，开始安装。
4. 安装成功后，会提示 Java 扩展安装成功的消息。

    > **说明：**
    >
    > 当您尝试录制未安装 Java 插件且无法自动注入的应用时，编辑器也会引导您安装 Java 插件。此时 Java 插件只会安装到当前录制的应用程序的 JRE 中。

## 使用命令行安装

1. **关闭所有 Java 应用，**  找到 Studio 安装目录下 JavaSupport 文件夹下的扩展安装程序 EncooJavaExtensionInstaller.exe。

   > **说明：**
   >
   > 针对不同版本的安装目录，可参考如下：
   >
   >- 1.1.2009.X 之前的版本的安装目录：`C:\Users\UserName\AppData\Local\Encoo\Encoo Studio\IDE\JavaSupport`，其中 `UserName` 为实际用户名。
   >- 1.1.2009.X 及之后的版本的安装目录：C:\Users\UserName\AppData\Local\Encoo Studio\app-x.x.xxxx.xx\Extensions\Java，其中 UserName 为实际用户名。

2. 以管理员权限打开命令行，切换到对应版本的安装目录路径，如，
   ```cd C:\Users\UserName\AppData\Local\Encoo Studio\app-x.x.xxxx.xx\Extensions\Java```

3. 执行安装命令：
   ``` EncooJavaExtensionInstaller.exe -install -a ```

## 手动安装

除了自动安装，我们依旧支持手动安装，以应对自动安装不工作的情况。

1. 找到编辑器或机器人安装目录下的JavaSupport文件夹。

   ![img](https://docimages.blob.core.chinacloudapi.cn/images/Amanda/Java/1.png)

   >**说明：**
   >
   > 1.1.2009.X及之后的版本为安装目录下的Extensions\Java文件夹。

2. 针对编辑器1.1.2009.X及之后的版本，将JavaSupport文件夹中accessibility.properties复制到runtime的\lib目录下，将JavaSupport文件夹中BotTimeJavaBridge.jar复制到runtime的\lib\ext目录下，然后将`BotTimeJavaBridge-*.dll`和`BotTimeJAWTBridge-*.dll`复制到`runtime的\bin\`目录下。（视runtime为32或64位复制相应后缀的dll）

   |扩展文件|目标路径|
   |---|---|
   |BotTimeJavaBridge-32/64.dll|%JAVAHOME%\bin|
   |BotTimeJAWTBridge-32/64.dll|%JAVAHOME%\bin|
   |accessibility.properties|%JAVAHOME%\lib|
   |BotTimeJavaBridge.jar|%JAVAHOME%\lib\ext|
   |jaccess.jar|%JAVAHOME%\lib\ext|

## EncooJavaExtensionInstaller工具

**EncooJavaExtensionInstaller**是用于在计算机上自动部署Java扩展的应用程序。它支持全盘扫描或者在特定目录安装/卸载Java插件。

>**注意：**
>
>- 建议使用管理员权限运行，以避免安装过程中出现的权限问题。
>- 安装或卸载之前建议关闭Java应用程序，以避免出现文件占用的问题。

### 安装

- EncooJavaExtensionInstaller.exe -install -a，全盘扫描JRE并安装Java插件，此操作可能比较慢。
- EncooJavaExtensionInstaller.exe -install -d，扫描默认位置(Program Files && Program Files (x86))的公用JRE并安装Java插件。
- EncooJavaExtensionInstaller.exe -install -p "specified path"，向特定的路径安装Java插件，路径可以是java.exe或者javaw.exe的路径或所在目录。

### 卸载

- EncooJavaExtensionInstaller.exe -uninstall -a，全盘扫描JRE并卸载已安装的Java插件，此操作比较耗时。
- EncooJavaExtensionInstaller.exe -uninstall -d，扫描默认位置(Program Files && Program Files (x86))的公用JRE并卸载已安装的Java插件。
- EncooJavaExtensionInstaller.exe -uninstall -p "specified path"，卸载特定的路径下已安装的Java插件，路径可以是java.exe或者javaw.exe的路径或所在目录。

## 常见问题

1. **提示“找不到32位/64位的Java运行环境”**

    Encoo找不到公共Java运行环境初始化Java扩展，需要按提示安装32位或64位的JRE。可以到以下地址下载对应版本的Java：<https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html>

    a）点击 Accept License Argument

   ![接受许可协议](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-acceptLicenseArguments.png)

    b) 按Encoo提示点击下载32位或64位的Java（x86为32位，x64为64位）

   ![下载java](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-downloadJava.png)

2. **对于Java Applet应用或无法attach的应用，需要手动安装Java扩展到runtime目录**

    a) 找到Studio或Robot安装目录下的JavaSupport文件夹

    ![查找JavaSupport文件夹](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-javaSupport.png)

    >**说明：**
    >
    > Robot在1.1.2010.17及以后的版本为安装目录下的Extensions\Java文件夹。

    b) 针对机器人在1.1.2010.17及以后的版本,将JavaSupport文件夹中accessibility.properties复制到runtime的\lib目录下，将JavaSupport文件夹中BotTimeJavaBridge.jar复制到runtime的\lib\ext目录下，    然后将`BotTimeJavaBridge-*.dll`和`BotTimeJAWTBridge-*.dll`复制到runtime的\bin\目录下。（视runtime为32或64位复制相应后缀的dll）
