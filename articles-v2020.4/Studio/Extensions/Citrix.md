# Citrix扩展

## 关于 Citrix 扩展

Citrix 广义上指 Citrix Desktop 和 Citrix App 两种虚拟化资源交付方式。

云扩 RPA 为提高自动化能力，已支持 Citrix 。用户只需在本地客户端安装 Encoo Citrix 扩展及远程服务端（Citrix Desktop 或 Citrix Apps）安装 EncooRemoteRuntime 后，像使用本地客户端一样，可以操作 Citrix 远程服务端的界面元素（如，“单击”、“输入文本”、“获取文本”等等界面自动化操作），使您在 Citrix Desktop 或 Citrix App上得到和原生自动化方式一样的体验，而无需使用图像识别等自动化技术。。







Citrix StoreFont(收藏夹、桌面、应用程序)

Citrix Desktop为远程虚拟桌面，类似于RDP




**支持的功能**如下：
在本地客户端和远程服务端安装对应的Citrix 扩展后，可执行以下操作：
- 为本地客户端和远程服务端中的用户界面元素生成选取器。

Citrix桌面支持    
Citrix应用程序支持



## 安装配置步骤

- **本地端安装 Citrix 扩展**
Citrix 扩展安装在本地计算机上，以使 Encoo Studio/Robot 以原生的方式自动化 Citrix 相关的应用程序。
**前提条件**
在本地计算机上安装 Citrix 客户端（即，Citrix Receiver 或 Citrix Workspace）
**操作步骤**
  1. 在编辑器的“**开始 > 工具**”页中获取本地端 Citrix 扩展。
  2. 单击**Citrix 扩展**，根据安装向导进行安装。
  3. 在弹出安装成功提示框后，重启所有 Citrix 连接，使得安装生效。
**后续操作**
  

- **远程服务端安装 EncooRemoteRuntime**
Encoo Remote Runtime为运行在 Citrix 服务器上的组件，可以使Citrix 远程桌面或远程应用程序与 Citrix 本地扩展进行通信，从而可以在本地产生选择器并执行自动化操作。 

**远程服务端安装 Web & Java 扩展**
   
当您需要在远程机器上自动化浏览器或者Java应用程序时，需要在服务器上安装对应的扩展，以取得更好的自动化支持。

1. Web 扩展安装
    - 找到RemoteRuntime安装目录下的Web扩展安装程序(Encoo.Web.ExtensionInstall.exe)，路径为："C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\Encoo.Web.ExtensionInstall.exe"
    - 打开命令行，执行命令 cd "C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\"，切换到安装程序所在目录
    - 根据需要安装的浏览器扩展，执行以下命令执行安装：
        1. Chrome浏览器

            Encoo.Web.ExtensionInstall.exe -install -t Chrome -l zh-CN

        2. FireFox浏览器

            Encoo.Web.ExtensionInstall.exe -install -t FireFox -l zh-CN

        3. Web360浏览器

            Encoo.Web.ExtensionInstall.exe -install -t Web360 -l zh-CN

        4. Microsoft Edge浏览器

            Encoo.Web.ExtensionInstall.exe -install -t Edge -l zh-CN

2. Java 扩展安装
    - 找到RemoteRuntime安装目录下的Java扩展安装程序(EncooJavaExtensionInstaller.exe)，路径为："C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\EncooJavaExtensionInstaller.exe"
    - 以管理员权限打开命令行，执行命令 cd "C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\"，切换到安装程序所在目录
    - 执行以下命令执行安装：

        EncooJavaExtensionInstaller.exe -install -a



   
   在控制台的**首页**的“安装包下载”中获取远程端 RemoteRuntime。

##  Citrix 操作示例


## 常见问题