# 删除区域

## 视频示例

## 概述

对指定工作表的单元格区域进行删除操作。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：执行删除操作的目标工作表。
- **区域** ：删除操作的目标单元格区域。
- **移动模式**：移动单元格的模式选择。包括: 下方单元格上移，右侧单元格左移，整行，整列。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：删除 Sheet1 工作表的 `"F2:F6"` 区域的数据，同时右侧单元格左移。

![配置删除区域组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Delete2.png)
