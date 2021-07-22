# 去重

## 视频示例

## 概述

对指定工作表区域去除重复值, 保留第一非空行数据，删除剩余行内容。

> **说明：**
>
> 该组件需在 Office Excel 的 **打开/新建** 组件内进行使用。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：执行去重操作的目标工作表。
- **区域** ：欲去重的单元格区域。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)
**此流程执行逻辑**：将指定工作表 Sheet2 中 A 列相同的单元格值进行去重。

![配置去重组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateCells2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateCells3.png)
