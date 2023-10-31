# 分列

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Split.mp4"></video>

## 概述

实现 Excel 工作表中某一列数据的分割，最终将该列数据拆成一列或多列数据显示。

> **说明：**
>
> 一般需搭配 “Office Excel > 打开/新建”组件进行使用。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表**：指定的需要分列的数据所在工作表。如，"Sheet1"。
- **列号**：指定的需要分列的数据所在工作表的列号，依赖于 "顺序" 中的列类型，支持数字或字母形式的列号，如，1、2、3、A、B、C等。
- **目标区域**：输入分列后数据的目标区域位置。如，"B1: C20"。
- **顺序**：下拉选择列号的类型：数字列号、字母列号。

  > **说明：**
  >
  >- 一般情况下，列号的类型是字母列号，如，A、B、C 等等。
  >- 通过勾选 Excel “选项 > 公式 > 使用公式”中的“R1C1 引用样式”，可设置列号类型为数字列号。

## 使用示例

**前置必要组件**：[打开/新建](../../TableExcelWPS/OpenExcel.md)

**此流程执行逻辑**：将指定工作表 Sheet1 中 A 列的数据以空格分割后，存放于“B1：B100”区域。

![配置分列属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/excelcolumn20201217.png)

**执行结果**：

![查看分列后的数据](https://docimages.blob.core.chinacloudapi.cn/images/Activities/excelcolumndataresult20201217.png)