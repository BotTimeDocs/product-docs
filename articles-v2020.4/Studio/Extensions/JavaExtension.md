# Jave扩展
适用于Java1.6及以上应用程序的自动化

  > 对于使用Java 9+ JRE 打开的应用程序： 在Java 9之前，JRE会包含attach模块，Java扩展依赖其对Java程序进行自动化。对于Java 9+，attach模块仅包含在JDK中，所以对于使用JRE9+打开的程序，需要手动在JRE目录下添加此模块



## 从编辑器安装
1. **关闭所有Java应用，** 点击编辑器左侧工具栏上“工具”图标
2. 选择“扩展 > Java扩展“后将会弹出确认窗口
3. 点击”确定“后，会以管理员权限启动Java扩展安装程序，点击用户账户控制窗口上的“是”，开始安装
4. 安装成功后，会提示Java扩展安装成功的消息

## 使用命令行安装
1. **关闭所有Java应用，**  找到Studio安装目录下JavaSupport文件夹下的扩展安装程序EncooJavaExtensionInstaller.exe。
 
   > **说明：**
   >针对不同版本的安装目录，可参考如下：
   > - 1.1.2009.X之前的版本的安装目录：“C:\Users\UserName\AppData\Local\Encoo\Encoo Studio\IDE\JavaSupport”，其中UserName为实际用户名。
   >  - 1.1.2009.X及之后的版本的安装目录：C:\Users\UserName\AppData\Local\Encoo Studio\app-x.x.xxxx.xx\Extensions\Java，其中UserName为实际用户名。

2. 以管理员权限打开命令行，切换到对应版本的安装目录路径，如，
   ```cd C:\Users\UserName\AppData\Local\Encoo Studio\app-x.x.xxxx.xx\Extensions\Java```

3. 执行安装命令：
   ```EncooJavaExtensionInstaller.exe -install -a```

**注：当您尝试录制未安装Java插件且无法自动注入的应用时，编辑器也会引导您安装Java插件。此时Java插件只会安装到当前录制的应用程序的JRE中。**


## 手动安装
除了自动安装，我们依旧支持手动安装，以应对自动安装不工作的情况

1. 找到编辑器或机器人安装目录下的JavaSupport文件夹。

   ![img](https://docimages.blob.core.chinacloudapi.cn/images/Amanda/Java/1.png)


   >**说明：**
   >
   > 1.1.2009.X及之后的版本为安装目录下的Extensions\Java文件夹。


1. 将JavaSupport文件夹中accessibility.properties复制到runtime的\lib目录下，将JavaSupport文件夹中BotTimeJavaBridge.jar复制到runtime的\lib\ext目录下，然后将BotTimeJavaBridge-*.dll和BotTimeJAWTBridge-*.dll复制到runtime的\bin\目录下。（视runtime为32或64位复制相应后缀的dll）
   
   >**说明：**
   >
   > 1.1.2009.X及之后的版本:
   > 将文件夹中accessibility.properties复制到runtime的\lib目录下，将文件夹中BotTimeJavaBridge.jar复制到runtime的\lib\ext目录下，然后将BotTimeJavaBridge-.dll和BotTimeJAWTBridge-.dll复制到runtime的\bin\目录下。

    |扩展文件|目标路径|
    |---|---|
    |BotTimeJavaBridge-32/64.dll|%JAVAHOME%\bin|
    |BotTimeJAWTBridge-32/64.dll|%JAVAHOME%\bin|
    |accessibility.properties|%JAVAHOME%\lib|
    |BotTimeJavaBridge.jar|%JAVAHOME%\lib\ext|
    |jaccess.jar|%JAVAHOME%\lib\ext|

## EncooJavaExtensionInstaller工具

EncooJavaExtensionInstaller是用于在计算机上自动部署Java扩展的应用程序。它支持全盘扫描或者在特定目录安装/卸载Java插件。

**注：建议使用管理员权限运行，以避免安装过程中出现的权限问题。**

**安装或卸载之前建议关闭Java应用程序，以避免出现文件占用的问题。**

### 具体用法：

1. 安装
    - EncooJavaExtensionInstaller.exe -install -a，全盘扫描JRE并安装Java插件，此操作可能比较慢。
    - EncooJavaExtensionInstaller.exe -install -d，扫描默认位置(Program Files && Program Files (x86))的公用JRE并安装Java插件。
    - EncooJavaExtensionInstaller.exe -install -p "specified path"，向特定的路径安装Java插件，路径可以是java.exe或者javaw.exe的路径或所在目录。

2. 卸载
    - EncooJavaExtensionInstaller.exe -uninstall -a，全盘扫描JRE并卸载已安装的Java插件，此操作比较耗时。
    - EncooJavaExtensionInstaller.exe -uninstall -d，扫描默认位置(Program Files && Program Files (x86))的公用JRE并卸载已安装的Java插件。
    - EncooJavaExtensionInstaller.exe -uninstall -p "specified path"，卸载特定的路径下已安装的Java插件，路径可以是java.exe或者javaw.exe的路径或所在目录。
