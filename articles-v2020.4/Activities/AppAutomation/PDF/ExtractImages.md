# 读取图片

## 视频示例

## 概述

可实现获取指定 PDF 文件中的图片

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **开始页码** ：输入被提取图片的 PDF 文件开始页码，若为空则从第一页开始读取。可接整型类型变量和整型
- **结束页码** ：输入被提取图片的 PDF 文件结束页码，若为空则为最后一页。可接整型类型变量和整型
- **图片名称前缀** ：输入提取的图片名称前缀。仅支持字符串变量和字符串

### 输入

- **文件路径** ：输入欲被提取图片的 PDF 文件路径。仅支持字符串变量和字符串
- **保存至文件夹** ：输入提取的图片被保存的文件夹目录。仅支持字符串变量和字符串

### 输出

- **图片路径列表** ：输出提取的图片路径列表

## 使用示例

1. 拖入 **读取图片** 组件至项目流程中，并设置变量 result(list <string>)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractImages_1.png)

2. 双击打开读取图片，选取 pdf，例："D:\\滴滴电子发票 (1).pdf"，选择需要的页数范围，输入保存文件夹，在输出中添加 list <string>, 如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractImages_2.png)

3. 点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractImages_3.png)