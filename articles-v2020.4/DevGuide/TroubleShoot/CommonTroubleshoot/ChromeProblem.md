# Chrome 扩展问题排查

## 限制条件

- 建议使用官方版本的 Chrome 浏览器，不推荐使用绿色版或论坛定制版的 Chrome 浏览器。
- Chrome 版本最低为 60。
- 在安装该扩展前，可能会要求你关闭 Google Chrome，因此请务必将处理中的相关任务进行保存。

## 常见排查步骤

1. **Chrome 录制失败，无法与 Chrome 扩展通信？**

    解决办法： 若出现无法与浏览器扩展通讯的提示，可按照如下步骤排查：

    (1) 检查 chrome 浏览器扩展，是否安装了 chrome 扩展并且启用，如果未安装“云扩录制器”扩展，需要 [通过 Studio 进行自动安装](./../../../Studio/Extensions/ChromeExtension.md)。

    ![步骤 1](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/chrome0120220506.png)

    (2) 当打开 chrome 后，检查“任务管理器”中是否存在 EncooNativeMessageHost.exe 进程：，该进程是 RPA 与 chrome 浏览器的通信进程，如果不存在，则检查(1)。

    > 说明：
    >
    > - **如果 EncooNativeMessageHost.exe 进程未启动**，需暂时关闭杀毒软件的防护功能，然后 通过 Studio 进行自动安装。
    > - **如果 EncooNativeMessageHost.exe 进程未启动且已经关闭杀毒软件并安装了扩展**，需暂时关闭杀毒软件的防护功能并删除“C:\Users\当前用户\AppData\Local\Encoo\messagehost”文件夹，然后再次通过 Studio 进行安装扩展。
    > - **如果杀毒软件暂时无法关闭，需要公司超级管理员授权才可关闭时**，请用可修改注册表的用户登录，手动修改注册表，手动安装 Chrome 扩展。

    ![步骤 2](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/chrome0220220506.png)
