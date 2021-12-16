# 输出数据表

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/OutDatatable.mp4"></video>

## 概述

将一个数据表按照选择的格式输出为字符串。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：要输出的数据表名，取此值代表的数据表并输出为字符串。

### 输出

- **输出**：将输出后的数据表存储到此变量。

### 可选项

- **输出格式** ：按照选择的格式将数据表输出为字符串。包含两个值：CSV、JSON。

## 使用示例

**前置必要组件**：[搭建数据表](../DataTable/BuildDataTable.md)

**此流程执行逻辑**：将已搭建的数据表`table`,以`CSV`形式输出至`csvstring`变量中。

![配置输出数据表组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OutputDataTable20201224.png)
