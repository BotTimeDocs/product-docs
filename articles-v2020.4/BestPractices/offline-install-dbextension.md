# 离线安装 IBM DB2 扩展

## 概述

本文解决的场景为“在只有公司内网或没有网络的情况下，如何安装 IBM DB2 扩展”。

## 操作思路

1. 在一台有网络的计算机中，下载 IBM DB2 扩展的安装包
2. 将下载下来的 IBM DB2 扩展的安装包文件拷贝至另一台无网络的计算机中
3. 从编辑器/机器人的扩展入口，单击 IBM DB2 扩展进行安装

![操作思路](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/offlineibmdb2.png)

## 前置条件

- 有一台有网络的计算机
- 有一台无网络的计算机并在该计算机上安装了云扩 RPA 编辑器/机器人

## 操作步骤

1. 在有网络的电脑上下载 [IBM DB2 扩展的安装包](https://share.weiyun.com/NXqMlQJN)。
2. 将下载的安装包复制到安装路径所在的目录下。
   - 编辑器中 IBM DB2 扩展的路径：`%UserProfile%\AppData\Local\Encoo Studio\app-x.x.xxxx.x\buildinActivities`
   - 机器人中 IBM DB2 扩展的路径：`%programfiles(x86)%\Encoo Robot\app-x.x.xxxx.x\buildinActivities`

3. 单击编辑器/机器人中的“IBM DB2 扩展”，进行安装。

    ![安装 IBM DB2](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/installibmdb2extension20220408.png)

## 常见问题

1. **Q：无法加载 DLL “db2app.dll”：找不到指定的模块**
    **A：** 排查步骤如下：

    a. 确认 DB2 扩展是否已经安装，若更新过编辑器或者机器人则需要重新安装 DB2 扩展。

    b. DB2 数据库访问驱动 DLL 需要 C++运行环境，一般新电脑没有 [C++环境](https://docimages.blob.core.chinacloudapi.cn/images/Studio/DataBase/RuntimePack.zip)，安装即可。

    c. 若以上步骤还是提示该问题，需要检查 Windows 系统版本，是否是 Windows Embedded Standard，根据系统是 64 位系统还是 32 系统下载安装。

    - x64 下载安装：<https://share.weiyun.com/FFxPWka7>
    - x86 下载安装：<https://share.weiyun.com/DBAnBZBe>
