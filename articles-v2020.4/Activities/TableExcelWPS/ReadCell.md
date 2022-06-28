# 读取单元格

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ReadCell.mp4"></video>

## 概述

获取工作簿单元格内数据并可存储在变量中

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：目标单元格所在工作表。
- **单元格** ：读取数据的目标单元格。

### 输出

- **单元格内容** ：将读取到的目标单元格内数据存储在此变量内。

### 可选项

- **保留格式** ：勾选时，将同时读取目标单元格的数据内容和数据格式（例如：货币，日期等），并在作为“写入单元格”的输入时，同时保持此数据格式；不勾选时，在“写入单元格”时使用默认“常规”数据格式。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：读取EXCEL“sheet1”中的“A1”单元格中的内容至“sheet1”中的“A2”单元格中。

![配置读取单元格组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCell1.png)

**后置必要组件**：[写入单元格](../OfficeExcel/WriteCell.md)
