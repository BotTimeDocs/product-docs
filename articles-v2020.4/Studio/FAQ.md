# FAQ

## 安装相关

1. **Q：安装时弹出程序崩溃提示，如图：**

   ![安装崩溃](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/installCollapse.png)

   **A：** 打开控制面板-> 程序-> 卸载程序，在卸载或更改程序列表中检查是否安装.Net Framework 4.6.1 及以上版本的.Net Framework 环境。如果未安装，请先下载.Net Framework 4.6.1 并安装，安装好之后重启电脑再进行云扩 RPA 编辑器的安装。下载地址：<https://www.microsoft.com/zh-CN/download/details.aspx?id=49982>

2. **Q：点击安装，显示安装失败**

   **A：** 检查当前用户在安装目录的读写权限，如果当前用户在安装路径没有读写权限，则要用管理员账号登录，在安装目录右键，点击属性，点击安全标签，添加目标账户，并添加完全控制权限，最后点击确定，然后退出管理员账号，用目标用户登录进行安装。

3. **Q：编辑器的默认安装目录是什么？**

   **A：** `%UserProfile%\AppData\Local\Encoo Studio`

4. **Q：机器人的默认安装目录是什么？**

   **A：** `%programfiles(x86)%\Encoo Robot`

## 卸载相关

1. **Q：卸载失败**

   **A：** </br>
   (1) 安装目录(Program files x86)，25 版本以后的安装目录在用户目录 AppData\Local\，下面 encootech 文件夹删掉 </br>
   (2) C:\ProgramData\Package Cache\ 里面搜一下 Digi4th 开头的 都删掉 </br>
   (3) 删除 windows 服务 DataBusService(cmd 命令行 sc delete DataBusService)

## 系统日志相关

1. **Q：编辑器 / 机器人的系统日志的默认路径是什么？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Log`。

2. **Q: 编辑器 / 机器人的安装日志的默认路径是什么？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Installation`。

## 市场相关

1. **Q: 从组件市场安装的组件包存放在本地计算机什么路径下？**

   **A：** `%UserProfile%\.nuget\packages`

## 插件相关

1. **Q: Chrome 录制失败，自动化失败有哪些原因？**

    **A：** </br>
    (1) 检查 chrome 浏览器扩展，是否安装了 chrome 插件并且启用，如图：

    ![启用扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/chrome-usingExtension.png)</br>

    (2) 当打开 chrome 后，检查任务管理器是否存在进程：EncooNativeMessageHost.exe，该进程是 RPA 与 chrome 浏览器的通信进程，如果不存在，则检查(1)。

    ![检查进程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/taskManager.png)</br>

1. **Q: 怎么安装 chrome 插件？**

    **A：** 打开编辑器，在**开始 > 工具 > 扩展** 中，选择并点击“Chrome扩展”，根据提示操作即可。（在安装后，请手动打开浏览器并输入：chrome://extensions/，启用扩展。）

    ![安装扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/extensioninpath20201019.png)
