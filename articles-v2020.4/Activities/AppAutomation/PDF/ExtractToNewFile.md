# 提取为新文档

## 视频示例

## 概述

可实现获取指定 PDF 文件中的数据并写入到新文件

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **文件同名替换** ：指定是否替换新文件所在目录下的同名文件

### 输入

- **文件路径** ：输入欲被提取数据的 PDF 文件路径。仅支持字符串变量和字符串
- **新文件路径** ：输入提取数据后写入的新文件路径。仅支持字符串变量和字符串
- **开始页码** ：输入被读取数据的 PDF 文件开始页码。可接整型类型变量和整型
- **结束页码** ：输入被读取数据的 PDF 文件结束页码。可接整型类型变量和整型

## 使用示例

1. 拖入 **提取为新文档** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractToNewFile_1.png)

2. 双击打开提取为新文档，选取 pdf，例："D:\\滴滴电子发票 (1).pdf"，选择需要的页数范围，输入生成路径，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractToNewFile_2.png)

3. 生成新文件为 "D:\\滴滴电子发票（3）.pdf"，点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractToNewFile_3.png)