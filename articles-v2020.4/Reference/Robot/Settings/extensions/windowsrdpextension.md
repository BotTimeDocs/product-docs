# Windows 远程桌面扩展（企业版）

安装 Windows 远程桌面扩展，以自动化远程桌面。

## 关于原生 RDP 自动化

远程桌面协议（RDP）是一种通过网络连接到其他计算机的常用方法。借助原生 RDP 自动化，您可以像在自己的计算机上一样生成选择器，并可在网络中的其他计算机上执行这些选择器的操作，而不必为其安装 RPA。如此一来，您便可轻松使用全部 "界面自动化" 组件，并从中受益。

## 安装配置步骤

若要获得原生 RDP 自动化支持，需执行以下几个步骤。执行完所有步骤后，您可使用客户机上的 Studio 在 "界面自动化" 组件和向导的帮助下构建流程。

### 设置客户端

1. 在 Studio 的 **开始 > 工具 > 扩展** 页面中， 找到“Windows 远程桌面扩展”。
2. 单击“Windows 远程桌面扩展”图标，以安装云扩 Windows 远程扩展程序，根据向导提示进行安装。

    ![Windows 远程桌面扩展入口](https://docimages.blob.core.chinacloudapi.cn/images/Studio/windowsrdp20210324.png)

### 设置远程桌面计算机

Encoo Remote Runtime 为运行在 RDP 远程端上的组件，可以使 RDP 远程桌面或远程应用程序与 RDP 本地扩展进行通信，从而可以在本地产生选择器并执行自动化操作。

1. 下载远程服务端 [Encoo Remote Runtime 安装包](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Encoo.RemoteRuntime.Setup.exe)。
2. 在需要自动化的 RDP 应用程序服务器上安装 Encoo Remote Runtime 安装包。
3. （可选）当您需要在远程机器上自动化浏览器或者 Java 应用程序时，需要在服务器上安装对应的扩展，以取得更好的自动化支持。

    - **Web 扩展安装**

      a. 找到 Remote Runtime 安装目录下的 Web 扩展安装程序(Encoo.Web.ExtensionInstall.exe)，路径为："C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\Encoo.Web.ExtensionInstall.exe"
      b. 打开命令行，执行命令 ` cd C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\`，切换到安装程序所在目录。
      c. 根据需要安装的浏览器扩展，执行以下命令执行安装：
       - Chrome 浏览器
           `Encoo.Web.ExtensionInstall.exe -install -t Chrome -l zh-CN`
       - FireFox 浏览器
            `Encoo.Web.ExtensionInstall.exe -install -t FireFox -l zh-CN`
       - Web 360 浏览器
            `Encoo.Web.ExtensionInstall.exe -install -t Web360 -l zh-CN`

       - Microsoft Edge 浏览器
            `Encoo.Web.ExtensionInstall.exe -install -t Edge -l zh-CN`

    - **Java 扩展安装**
      a. 找到 RemoteRuntime 安装目录下的 Java 扩展安装程序(EncooJavaExtensionInstaller.exe)，路径为："C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\EncooJavaExtensionInstaller.exe"
      b. 以 **管理员权限** 打开命令行，执行命令 `cd C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\`，切换到安装程序所在目录
      c. 执行以下命令执行安装：
        `EncooJavaExtensionInstaller.exe -install -a`

安装完成后，您即可在远程桌面计算机上执行操作。

## 卸载 RDP

卸载本地 Windows 远程桌面扩展
  在本地计算机的注册表中，找到 `HKEY_CURRENT_USER\Software\Microsoft\Terminal Server Client\Default\AddIns\EncooRemotePluginRdp` 注册表值，删除后重启连接。

## 常见问题

1. **Q：是否支持远程桌面中再开远程的场景？**

   **A：** 暂不支持
