# Citrix扩展（企业版）

## 关于 Citrix 技术自动化

Citrix 广义上指 Citrix Desktop 和 Citrix App 两种虚拟化资源交付方式。

云扩 RPA 为提高自动化能力，已支持 Citrix 。用户只需在本地客户端安装 Encoo Citrix 扩展及远程服务端（Citrix Desktop 或 Citrix Apps）安装 Encoo Remote Runtime 后，像使用本地客户端一样，可以操作 Citrix 远程服务端的界面元素（如，“单击”、“输入文本”、“获取文本”等等界面自动化操作），使您在 Citrix Desktop 或 Citrix App上得到和原生自动化方式一样的体验，而无需使用图像识别等自动化技术。

**支持的功能**如下：
安装Encoo Citrix 扩展程序和 Encoo Remote Runtime 后，可执行以下操作：
- 为 Citrix Apps 和 Desktops 中的用户界面元素生成选择器。
- 可以使用界面自动化组件。
- 对使用 Citrix Apps 打开的浏览器执行自动化。

## 安装配置步骤

### 前提条件
在本地计算机上安装 Citrix 客户端（即，[Citrix Receiver](https://www.citrix.com/downloads/citrix-receiver/) 或 [Citrix Workspace](https://www.citrix.com/downloads/workspace-app/)）。

### 配置本地客户端

Citrix 扩展安装在本地计算机上，以使 Encoo Studio/Robot 以原生的方式自动化 Citrix 相关的应用程序。

1. 在编辑器中的“**开始 > 工具**”页中，获取本地端 Encoo Citrix 扩展。
2. 单击**Citrix 扩展**，根据安装向导进行安装。
   ![安装 Citrix 扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixpath20210107.png)

### 配置远程服务端

Encoo Remote Runtime为运行在 Citrix 服务器上的组件，可以使Citrix 远程桌面或远程应用程序与 Citrix 本地扩展进行通信，从而可以在本地产生选择器并执行自动化操作。

1. 在控制台中的“**首页 > 安装包下载**”中，获取远程服务端 Encoo Remote Runtime 安装包。
2. 在需要自动化的 Citrix 应用程序服务器上安装 Encoo Remote Runtime 安装包。
3. （可选）当您需要在远程机器上自动化浏览器或者 Java 应用程序时，需要在服务器上安装对应的扩展，以取得更好的自动化支持。

    - **Web 扩展安装**
 
      a. 找到 Remote Runtime 安装目录下的 Web 扩展安装程序(Encoo.Web.ExtensionInstall.exe)，路径为："C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\Encoo.Web.ExtensionInstall.exe"
      b. 打开命令行，执行命令` cd C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\`，切换到安装程序所在目录。
      c. 根据需要安装的浏览器扩展，执行以下命令执行安装：
       - Chrome 浏览器
           `Encoo.Web.ExtensionInstall.exe -install -t Chrome -l zh-CN`
       - FireFox 浏览器
            `Encoo.Web.ExtensionInstall.exe -install -t FireFox -l zh-CN`
       - Web 360浏览器
            `Encoo.Web.ExtensionInstall.exe -install -t Web360 -l zh-CN`

       - Microsoft Edge浏览器
            `Encoo.Web.ExtensionInstall.exe -install -t Edge -l zh-CN`

    - **Java 扩展安装**
      a. 找到 RemoteRuntime 安装目录下的 Java 扩展安装程序(EncooJavaExtensionInstaller.exe)，路径为："C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\EncooJavaExtensionInstaller.exe"
      b. 以**管理员权限**打开命令行，执行命令 `cd C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\`，切换到安装程序所在目录
      c. 执行以下命令执行安装：
        `EncooJavaExtensionInstaller.exe -install -a`


### 重新启动组件的 Citrix 会话

安装 Encoo Remote Runtime 和 Encoo Citrix 扩展程序后，需重新启动 Citrix 组件会话，更改才会生效。

1. 右键单击 Citrix Receiver 托盘图标，然后单击“连接中心”。

   ![重启生效](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixreceiver20210107.png)

2. 在弹出的“Citrix 连接中心”窗口中，选择组件会话，然后单击“注销”按钮。

   >**说明：**
   >
   >需为所有组件会话执行此操作。

3. 单击“关闭”按钮，确认所有更改并关闭窗口。

## 卸载 Citrix

- 卸载本地客户端 Encoo Citrix 扩展
  将本地计算机上，该路径`C:\Program Files (x86)\Citrix\ICA Client\`下的`EncooRemotePluginCitrix.dll`文件手动删除即可。

- 卸载远程服务端 Encoo Remote Runtime 程序
  在控制面板中与正常卸载程序一样，卸载`Encoo Remote Runtime 程序`即可。

##  Citrix 操作示例

为了展示 Citrix 技术自动化的工作方式，创建一个简单的自动化流程，该流程用于从浏览器中抓取网页数据后，保存到记事本中并修改字体。

1. 在本地客户端的编辑器中搭建一个获取远程服务端网页中的结构化数据的流程保存至远程服务端的记事本中并修改字体样式。
![Citrix Demo](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixdemo20210108.png)

2. 保存并运行流程，查看运行结果。
![Citrix 演示结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixdemoresult20210108.png)

## 常见问题

1. **Q：安装 Encoo Remote Runtime 程序后为何无法进行 Citrix 自动化操作？**
   **A：** 
   - Encoo Remote Runtime 程序需与本地客户端使用的自动化组件版本相对应，否则无法正常工作。
     >**说明：**
     >- 本地客户端使用的**自动化组件版本**在项目面板中的依赖项查看。
     >- 远程服务端使用的 **Encoo Remote Runtime 程序版本**在下载安装包时可查看。

    - 若编辑器或机器人升级后，Encoo Remote Runtime 程序也需升级至对应的版本，否则无法正常工作。

2. **Q：为何设置了 Citrix 的“首选项 > 显示”后，Web 元素指定元素时的定位发生偏移，桌面元素在窗口滚动后验证仍会高亮显示在原位置？**
   **A：** 当前 Encoo Remote Runtime 仅支持工作在“最佳分辨率”之上，遇到此现象时，需在 Citrix 的“首选项 > 显示”中设置"最佳分辨率"。
   ![最佳分辨率](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixproblem20210108.png)