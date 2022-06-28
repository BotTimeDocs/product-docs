# 替换

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Replace.mp4"></video>

## 概述

实现在指定 Office Excel 工作表的指定单元格范围内，输入查找的内容并替换为新内容。

> **说明：**
>
> 该组件需在 Office Excel 的 **打开/新建** 组件内进行使用。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **查找内容**：需要查找的内容。
- **工作表**：执行查找操作所在的工作表。
- **区域**：执行替换操作的单元格区域。当此项为空时，默认查找全表。可填单个单元格。
- **替换为**：需要替换的新内容。

### 可选项

- **单元格匹配**：默认不勾选；勾选后需完整匹配单元格内容，相当于精确完整匹配单元格的内容。
- **匹配大小写**：默认不勾选；勾选后需匹配内容大小写。
- **替换方式**：下拉选择替换方式，支持“全部替换”和“替换第一个”。
  - **全部替换（默认）**：替换查找的所有内容。
  - **替换第一个**：仅替换查找的第一个。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：将一个名叫 test 的 Excel 中的“语”字替换为“文”字。

![查找替换](https://docimages.blob.core.chinacloudapi.cn/images/Activities/officeexcelreplace20210224.png)

**执行结果**：

![流程执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/officeexcelreplaceresultdata20210224.png)
