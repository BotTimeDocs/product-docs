# 读取Excel文件


## 概述

读取Excel文件中的工作表，并存储到数据表变量。支持xls、xlsx、et、ett格式文件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件路径**：操作的Excel文件路径，包括该Excel文件名。
- **工作表**：读取的Excel工作表名称。

### 输出

- **数据表** ：将读取到的数据存储在此变量，仅支持DataTable类型。

### 可选项

- **添加列头** ：勾选时，将工作表的第一行设为数据表的列头。

## 使用示例

**前置必要条件**：输入属性正确

**此流程执行逻辑**：读取一个Excel文件，并预览读取到的结果。

![读取Excel文件](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dtexcel001.png)
