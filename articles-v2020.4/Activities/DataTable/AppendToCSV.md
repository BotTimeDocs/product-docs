# 追加到 CSV 文件

## 视频示例

## 概述

将数据表追加到已有 CSV 文件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将此数据表追加到已有 CSV 文件。
- **文件路径** ：CSV 文件路径，若不存在则新建。支持相对和绝对路径。需提供文件名且带后缀。例如：“E:\DT.csv”。无后缀则视为文件夹，即没有提供文件名，报错。如果有文件夹不存在，则新建。

### 可选项

- **分隔符** ：目标 CSV 文件的分隔符。此属性可不填写，默认使用逗号。
- **编码方式** ：文件的编码方式，默认为目标 CSV 文件的编码方式。

## 使用示例

**前置必要条件**：已有一个已搭建的数据表，可参见 [搭建数据表](../DataTable/BuildDataTable.md)。

**此流程执行逻辑**：将已搭建的数据表 `table` 追加至指定的 CSV 文件 `"C:\云扩科技\appendtocsv.csv"` 中。

![配置追加到 CSV 文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AppendToCSV2020122902.png)
