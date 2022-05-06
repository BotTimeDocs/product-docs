# 编辑器/机器人安装失败

## 限制条件

在安装编辑器或机器人客户端应用程序时，有如下几点需要注意：

- 安装前：
  
    - 需要Win 7 SP1及以上操作系统
    - 需要提前安装`.NET Framework 4.6.2`及以上版本
    - 在控制台首页中下载最新版本的编辑器或机器人的安装包

- 安装时：
    - 关闭杀毒软件
    - 使用管理员权限安装

## 常见排查步骤

常见的安装失败时的问题排查步骤：

1. **编辑器或机器人安装失败**

    ![安装失败](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/install20220506.png)

    解决办法：

    - Step1：检查杀毒软件是否正在运行，如果正在运行则需要将杀毒软件(如，360 软件)关闭后重新安装编辑器或机器人。

    - Step2：检查当前用户在安装目录的读写权限，如果当前用户在安装路径没有读写权限，则需用管理员账号登录，在安装目录处右键，点击属性，点击安全标签，添加目标账户，并添加完全控制权限，最后点击确定，然后退出管理员账号，用目标用户登录进行安装。

2. **编辑器或机器人安装时报.NET错误**

    ![net错误](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/net20220506.png)

    解决办法：

    - Step1：在“控制面板 > 程序 > 卸载程序”中检查是否安装`.NET Framework`环境

    - Step2：如果未安装，则
需要下载并安装`.NET Framwork 4.2`(<https://dotnet.microsoft.com/zh-cn/download/dotnet-framework>)及以上的版本

    - Step3：安装好之后重启电脑再进行云扩RPA编辑器或机器人的安装