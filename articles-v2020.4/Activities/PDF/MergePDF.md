# 合并文件

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/MergeFile.mp4"></video>

## 视频示例

## 概述

可实现对多个 PDF 文件合并为一个 PDF 文件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **原文件路径** ：输入或选择欲被合并的文件路径列表；点击 "..." 打开弹窗选择文件后可自动生成文件列表数组。可接 IEnumerable 类型变量和对象，例如：数组或集合
- **新文件路径** ：合并后的文件路径。

### 可选项

- **文件同名替换** ：指定是否替换新文件所在目录下的同名文件。

## 使用示例

**此流程执行逻辑**：将"D:\\滴滴电子发票 (1).pdf"和 "D:\\滴滴电子发票.pdf"进行合并，生成新的文件为 "D:\\滴滴电子发票（2）.pdf"。

![配置合并文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergePDF_2.png)
