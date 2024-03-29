# 下载文件

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/DownLoadFile.mp4"></video>

## 概述

此组件可以发送下载请求并输出文件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **URL** ：输入请求的URL。
- **保存至目录** ：输入文件将被下载到的目录，若为空则默认为Windows的下载目录。
- **超时(秒)** ：输入请求超时秒数。
- **同名覆盖** ：输入是否覆盖当前路径的同名文件。

### 输出

- **文件路径** ：输出下载的文件本地路径。

## 使用示例

**此流程执行逻辑**：下载指定URL`"https://dtapp-pub.dingtalk.com/dingtalk-desktop/win_installer/Release/DingTalk_v5.1.41.19.exe"`中的文件并保存至目录`"D:\下载"`中。

![配置下载文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPDownload1.png)

## 常见问题

1. **Q：下载图片能否使用“下载文件”组件？将变量放在“URL”属性处会报错**

    **A：** 这个变量是数据表，包含多个图片地址，详情可参见[用下载文件组件下载图片时变量报错的问题](https://v.qq.com/x/page/g326827dl22.html)。
