# 文件/路径是否存在

## 视频示例

## 概述

判断手机端中的指定文件/路径是否存在。

> **说明：**
>
> 该组件仅 Android 端支持。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **路径**：手机端中文件的路径或目录路径地址，如，`"/sdcard/DCIM/Camera/IMG_20211215_130018.jpg"`。
- **路径类型**：选择文件或目录的路径的类型。

>**说明：**
>
> 文件或目录的路径地址，可在计算机端的 cmd 命令提示符中，依次使用 `adb shell`、`ls` 等命令查看。

### 输出

- **结果**：将执行的结果存储至此变量中。

## 使用示例

**前置必要组件**：[连接设备](../../PhoneAutomation/MobileConnect.md)

**此流程执行逻辑**：判断手机中的 `"/sdcard/DCIM/Camera/IMG_20211215_130018.jpg"` 文件路径是否存在，结果保存至变量 `result` 中。

![配置流程](https://docimages.blob.core.chinacloudapi.cn/images/Activities/filepathexists20211215.jpg)
