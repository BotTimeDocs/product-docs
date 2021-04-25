# 基本操作

顶部操作栏罗列了应用的基本操作，你可以在顶部操作栏设置主题、保存、预览、发布应用。

## 主题管理

可以选择主题进行应用的美化。

在顶部导航区域，单击“主题”图标后，可对主题进行选择，默认主题为第一个主题。

![应用主题](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/them20210422.png)

## 布局展示

ViCode 应用支持 Web 端和移动端的页面布局的自适应展示。

![布局展现形式](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/showways20210425.png)

## 试运行应用

当你编辑好应用的全部信息，想要尝试运行一下你创建的应用。
点击预览，即可打开应用模拟运行界面。

![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/runApps1.png)

这个界面将展示用户实际打开应用时面对的内部交互页面，你可以在该页面验证你的配置是否生效。同时，当你点击提交后，我们将会带着你填写的参数，向机器人发送流程运行命令。

![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/runApps2.png)

## 发布应用

当应用已经编辑完毕，你想要将应用发布到控制台上，点击发布按钮。
发布前，系统将会校验你的应用是否存在编译错误。
若有，则系统会提示你错误信息，请根据错误信息修改错误的配置信息.

全部信息通过编译后，系统将自动检测当前应用在控制台对应资源组中被发布的最新版本，你可以在已有版本基础上叠加版本，最新版本号上填写的版本即为本次发布版本。
版本号可以向上叠加，但不允许小于当前版本号。
填写完全部数据后，点击发布，系统将会自动保存当前版本并将应用发布至控制台。
发布成功后，将会提示成功信息。

![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/publicapps.png)
