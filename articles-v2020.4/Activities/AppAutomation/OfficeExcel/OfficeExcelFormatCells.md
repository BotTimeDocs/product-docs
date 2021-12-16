# 设置单元格格式

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SetCellsFormat.mp4"></video>

## 概述

在 Excel 中，设置对指定单元格或单元格区域中数据的格式。支持的单元格式与 Excel 中支持的格式相同，如，常规、数值、货币、日期，等等。

> **说明：**
>
> 此组件需包含在“打开/新建”组件中。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表**：指定欲设置单元格格式的工作表名称。如，`"Sheet1"`。
- **区域/列号**：指定欲设置格式的单元格区域或单个字母列号。如，`"A1"`， `“A1:B9”`。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：将 Sheet1 中的 A1 至 C7 单元格区域中的数据，设置为保留 2 位小数的数值类型。

![配置设置单元格格式组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingcellformat20210611.png)

**执行结果**：

![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/runresult20210611.png)
