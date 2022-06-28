# 提取为新文档

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/AsNewDocument.mp4"></video>

## 概述

获取指定 PDF 文件中的数据并写入到新文件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件路径** ：输入欲被提取数据的 PDF 文件路径。
- **新文件路径** ：输入提取数据后写入的新文件路径。
- **开始页码** ：输入被读取数据的 PDF 文件开始页码。
- **结束页码** ：输入被读取数据的 PDF 文件结束页码。

### 可选项

- **文件同名替换** ：指定是否替换新文件所在目录下的同名文件。

## 使用示例

**此流程执行逻辑**：将 "D:\\滴滴电子发票 (1).pdf" 文件的第一页中的全部内容，提取为一个新文档保存为 "D:\\滴滴电子发票（3）.pdf"。

![配置提取为新文档组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractToNewFile_2.png)
