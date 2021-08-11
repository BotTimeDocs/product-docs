# 执行宏

## 视频示例

## 概述

执行外部宏文件或者 XLSM 格式的内部宏，支持实参传递。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **Sub/Function 名** ：执行宏的方法名。内部宏和外部宏均需填充此项。
- **传入实参** ：传入宏文件的实参。
- **宏文件路径** ：执行此外部宏文件。为空时，默认执行工作表内部宏。

### 输出

- **返回值** ：将宏执行后返回的值存储在此变量，前提为执行宏后有返回值。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：在 Excel 中执行指定的宏。

![宏文件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExecuteMacro3.png)

![配置执行宏组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExecuteMacro1.png)

**执行结果**：
在“输出面板”日志中打印所有 sheet 名称。
