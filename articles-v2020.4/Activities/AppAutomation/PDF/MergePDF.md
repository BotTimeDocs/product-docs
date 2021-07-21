# 合并文件

## 视频示例

## 概述

可实现对多个 PDF 文件合并为一个 PDF 文件

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **文件同名替换** ：指定是否替换新文件所在目录下的同名文件

### 输入

- **原文件路径** ：输入或选择欲被合并的文件路径列表；点击 "..." 打开弹窗选择文件后可自动生成文件列表数组。可接 IEnumerable 类型变量和对象，例如：数组或集合
- **新文件路径** ：对此列进行排序操作。填入列索引（例：1，即对第一列进行排序）。仅支持字符串变量和字符串

## 使用示例

1. 拖入 **合并文件** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergePDF_1.png)

2. 双击打开选定 pdf 文件（在弹框中一次选多个），例："D:\\滴滴电子发票 (1).pdf", "D:\\滴滴电子发票.pdf"，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergePDF_2.png)

3. 生成新文件为 "D:\\滴滴电子发票（2）.pdf"，点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergePDF_3.png)