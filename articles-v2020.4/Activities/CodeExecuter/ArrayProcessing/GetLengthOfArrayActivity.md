# 获取数组长度

## 视频示例

## 概述

获取指定数组的长度

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数组** ：输入欲被获取长度的数组

### 输出

- **长度** ：输出数组的长度；仅可接Int变量

## 使用示例

1. 拖入**获取数组长度**组件，设置变量`数组`，变量类型为`String[]`，默认值`new string[]{"A","B","C"}`，设置int变量`数组length`，**输入**数组变量`数组`，**输出**长度变量`数组length`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfArrayActivity1.png)
2. 拖入**写入日志**组件，打印`数组`的长度，输入**日志内容**`数组length.ToString()`，打印结果为`3`：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfArrayActivity2.png)
