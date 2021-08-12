# 查找

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Search.mp4"></video>

## 概述

在特定单元格区域内查找给定值，并返回第一个查找到的单元格地址。

> **说明：**
>
> 该组件需在 Office Excel 的 **打开/新建** 组件内进行使用。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **查找内容** ：取此值进行查找。
- **工作表** ：执行查找操作的目标工作表。
- **区域** ：查找操作的目标单元格区域，为空时，默认查找全表。

### 输出

- **单元格地址** ：将查找到的第一个单元格地址存储在此变量。

### 可选项

- **单元格匹配**：精确完整匹配单元格内容。
- **匹配大小写**：匹配查找内容大小写。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：查找指定工作表 Sheet2 中的值为 100 的单元格所在地址。

![配置查找组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Search2.png)
