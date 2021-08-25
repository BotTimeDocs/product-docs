# 保存为CSV文件

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SaveAsCsvFile.mp4"></video>

## 概述

将数据表保存为CSV文件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将此数据表保存为CSV文件
- **文件路径** ：保存的CSV文件路径。支持相对和绝对路径。需提供文件名且带后缀。例如：“E:\DT.csv”。无后缀则视为文件夹，即没有提供文件名，报错。如果有文件夹不存在，则新建。

### 可选项

- **分隔符** ：指定CSV文件的分隔符。此属性可不填写，默认使用逗号。
- **编码方式** ：文件的编码方式。可以在 [此处](../Appendix/Encoding.md) 找到每个字符编码的完整代码列表。要指定要使用的编码类型，请使用“名称”字段中的值。如果未指定编码类型，则默认为UTF-8。

## 使用示例

**前置必要组件**：[搭建数据表](../DataTable/BuildDataTable.md)

**此流程执行逻辑**：将已搭建的数据表`table`保存为"C:\云扩科技\savetable.csv"。

![配置保存为CSV文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SaveToCSV20201229.png)
