# 获取页数

## 视频示例

## 概述

可实现获取指定 PDF 文件的总页数

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件路径** ：输入欲被获取页数的 PDF 文件路径。仅支持字符串变量和字符串

### 输出

- **总页数** ：输出 PDF 文件的总页数

## 使用示例

1. 拖入 **获取页数** 组件至项目流程中，并设置变量 page_num(int32)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetPageNumbers_1.png)

2. 双击打开获取页数，选取 pdf，例："D:\\滴滴电子发票 (1).pdf"，选择需要的页数范围，输入生成路径，在输出中添加 page_num, 如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetPageNumbers_2.png)

3. 点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetPageNumbers_3.png)