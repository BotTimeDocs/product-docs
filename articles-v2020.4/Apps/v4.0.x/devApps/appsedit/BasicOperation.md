# 基本操作

顶部操作栏罗列了应用的基本操作，你可以在顶部操作栏设置全局变量、保存、预览、发布应用。

## 变量管理

### 概述

用于展示和管理应用的变量，每个应用独享一套变量且均为全局变量，应用之间不共享变量。

在 **应用开发** 模块的编辑模式中，单击“**变量**”，可对全局变量进行增删改查等操作。

![变量](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/globalvarible20210127.png)

### 示例

新增一个全局变量，且将该变量使用至应用中。

1. 在 **应用开发** 模块的编辑模式中，单击“变量”，并新增一个全局变量，如，`A=test`。

2. 在画布中拖入任一可绑定变量的组件，并配置其文本属性为已定义的变量。

    ![变量应用](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/checkbox20210127.png)

3. 单击 **预览**，查看效果。

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
