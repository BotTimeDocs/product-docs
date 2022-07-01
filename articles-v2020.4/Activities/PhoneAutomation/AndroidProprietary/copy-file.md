# 复制手机文件

## 视频示例

## 概述

将本手机中的文件复制到本地计算机中。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **本地文件路径**：将手机中的文件存放于计算机端的存储路径，如，`"C:\Users\wangxin\Desktop"`。
- **手机文件路径**：手机文件的存储路径，如，`"/sdcard/DCIM/Camera/IMG_20211215_130018.jpg"`。

    > **说明：**
    >
    > 手机文件的路径，可在计算机端的 cmd 命令提示符中，依次使用 `adb shell`、`ls` 等命令查看。

## 使用示例

**前置必要组件**：[连接设备](../../PhoneAutomation/MobileConnect.md)

**此流程执行逻辑**：将本手机中的 `"/sdcard/DCIM/Camera/IMG_20211215_130018.jpg"` 文件复制到本地计算机的桌面中 `"C:\Users\wangxin\Desktop"`。

![配置流程](https://docimages.blob.core.chinacloudapi.cn/images/Activities/copyfile20211215.jpg)
