# 读取图片

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ReadImage.mp4"></video>

## 概述

可实现获取指定 PDF 文件中的图片。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件路径** ：输入欲被提取图片的 PDF 文件路径。
- **保存至文件夹** ：输入提取的图片被保存的文件夹目录。

### 输出

- **图片路径列表**：输出提取的图片路径列表。

### 可选项

- **开始页码** ：输入被提取图片的 PDF 文件开始页码，若为空则从第一页开始读取。
- **结束页码** ：输入被提取图片的 PDF 文件结束页码，若为空则为最后一页。
- **图片名称前缀** ：输入提取的图片名称前缀。

## 使用示例

**此流程执行逻辑**：读取"D:\\滴滴电子发票 (1).pdf"文件的第一页中的图，识别后的图片保存到D盘路径下。

![配置读取图片组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractImages_2.png)
