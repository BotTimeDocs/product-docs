# 下载文件

## 视频示例

## 概述

此组件可以发送下载请求并输出文件

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **URL** ：输入请求的URL；仅支持字符串变量和字符串
- **保存至目录** ：输入文件将被下载到的目录，若为空则默认为Windows的下载目录；仅支持字符串变量和字符串
- **超时(秒)** ：输入请求超时秒数；仅支持整型变量和整型值
- **同名覆盖** ：输入是否覆盖当前路径的同名文件

### 输出

- **文件路径** ：输出下载的文件本机路径；仅支持变量
## 使用示例

1. 拖入**HTTP下载**组件，设置文件路径变量`path`，变量类型为`String`，**输入**URL`"https://dtapp-pub.dingtalk.com/dingtalk-desktop/win_installer/Release/DingTalk_v5.1.41.19.exe"`，**输入**保存至目录`"D:\下载"`，**输入**超时（秒）`300`，**输出**文件路径`path`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPDownload1.png)
2. 下载文件成功
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPDownload2.png)
3. 拖入**写入日志**组件，打印文件绝对路径，输入**日志内容**`path`，打印结果为`D:\下载\DingTalk_v5.1.41.19.exe`：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPDownload3.png)
