# 合并单元格

## 视频示例

## 概述

对指定单元格区域进行合并操作。

>**说明：**：
>
>此组件仅可在“打开/新建”组件中使用。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：指定欲进行合并单元格操作所属工作表名称。
- **区域** ：指定欲进行合并单元格区域。

### 输出

- **合并值**：合并后单元格的值。

    >**说明：**
    >
    >- 若合并单元格区域中只有一个值，则默认输出此唯一值；
    >- 若合并单元格区域中有多个值，则输出第一个非空单元格中的值。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：合并指定“Sheet2”工作表中的“A1: A3”单元格区域。

![配置合并单元格组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells3.png)
