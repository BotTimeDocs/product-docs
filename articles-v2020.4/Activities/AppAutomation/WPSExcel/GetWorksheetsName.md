# 获取所有工作表名

## 视频示例

## 概述

获取工作簿内所有工作表名称。

>**说明：**
>
>此组件仅可在“打开/新建”组件中使用，默认取其工作簿，无需再次输入。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **工作表名称** ：工作簿内所有工作表名存储到此变量。可结合循环组件输出或使用工作表名。

## 使用示例

**前置必要组件**：[打开/新建](../WPSExcel/OpenExcel.md)

**此流程执行逻辑**：获取`wps.xlsx`工作簿中所有的工作表名称，存储至`sheetlist`变量中。

![配置获取所有工作表名组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps41.png)
