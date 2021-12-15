# 推送文件到手机

## 视频示例

## 概述

将本地计算机端中的文件复制到手机端的指定路径下。

## 属性

### 基本

参见 [通用配置项](./../../Appendix/CommonConfigurationItems.md)。

### 输入

- **本地文件路径**：本地计算机端的文件路径，如，`"C:\Users\wangxin\Desktop\test.jpg"`。
- **手机文件路径**：需要存储至手机端中的存储路径，如，`"/sdcard/DCIM/Camera"`。

    > **说明：**
    >
    > 手机文件的路径，可在计算机端的 cmd 命令提示符中，依次使用 `adb shell`、`ls` 等命令查看。

## 使用示例

**前置必要组件**：[连接设备](./../MobileConnect.md)

**此流程执行逻辑**：将本地计算机端的 `"C:\Users\wangxin\Desktop\test.jpg"` 文件复制到手机端的相册中 `"/sdcard/DCIM/Camera"`。

![配置流程](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pushfile20211215.jpg)
