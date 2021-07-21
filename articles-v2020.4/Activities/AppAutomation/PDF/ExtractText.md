# 读取文本

## 视频示例

## 概述

可实现获取指定 PDF 文件中的文本

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **开始页码** ：输入被读取文本的 PDF 文件开始页码，若为空则从第一页开始读取。可接整型类型变量和整型
- **结束页码** ：输入被读取文本的 PDF 文件结束页码，若为空则为最后一页。可接整型类型变量和整型

### 输入

- **读取角度** ：指定读取时文件旋转的角度
- **文件路径** ：输入欲被提取文本的 PDF 文件路径。仅支持字符串变量和字符串

### 输出

- **结果** ：输出读取的文本数据。仅支持字符串变量

## 使用示例

1. 拖入 **读取文本** 组件至项目流程中，并设置变量 result(String)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractText_1.png)

2. 双击打开读取文本，选取 pdf，例："D:\\滴滴电子发票 (1).pdf"，选择需要的页数范围，输入生成路径，在输出中添加变量 result, 如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractText_2.png)

3. 点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractText_3.png)