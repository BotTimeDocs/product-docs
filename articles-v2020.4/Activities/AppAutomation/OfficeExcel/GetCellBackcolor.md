# 获取单元格背景色

## 视频示例

<video controls height='450px' width='800px' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetCellsBackground.mp4"></video>

## 概述

提取指定单元格的背景色，并返回十六进制值。同时可使用返回值作为“设置单元格背景色”组件的输入。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：指定目标单元格所属工作表名称。
- **单元格** ：提取背景色的目标单元格，不支持单元格区域（填入区域时将无法执行）。

### 输出

- **颜色** ：输出指定单元格背景色，例如 "#FFFFFF"。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：获取“Sheet1”工作表中“A1”单元格的背景色，存储至“color”变量中。

![配置获取单元格背景色组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetCellBackColor1.png)
