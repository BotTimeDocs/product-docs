# 下载文件

## 视频示例

## 概述

此组件可以发送下载请求并输出文件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **URL** ：输入请求的URL。
- **保存至目录** ：输入文件将被下载到的目录，若为空则默认为Windows的下载目录。
- **超时(秒)** ：输入请求超时秒数。
- **同名覆盖** ：输入是否覆盖当前路径的同名文件。

### 输出

- **文件路径** ：输出下载的文件本机路径。

## 使用示例

**此流程执行逻辑**：下载指定URL`"https://dtapp-pub.dingtalk.com/dingtalk-desktop/win_installer/Release/DingTalk_v5.1.41.19.exe"`中的文件并保存至目录`"D:\下载"`中。

![配置下载文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPDownload1.png)
