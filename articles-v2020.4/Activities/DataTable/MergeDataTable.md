# 合并数据表

## 视频示例

## 概述

将数据表按照指定规则进行合并，并将合并后的结果更新到目标数据表中。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **目标数据表** ：将源数据表合并到此表，此表存储合并后的数据。
- **源数据表** ：取此表数据合并到目标数据表，此表数据不会被更改。
- **结构不同时** ：执行合并操作的两表结构不同时，取此项来执行合并操作实现数据的取舍。

## 使用示例

**前置必要条件**：已有两个已搭建的数据表，可参见 [搭建数据表](../DataTable/BuildDataTable.md)。
**此流程执行逻辑**：将源数据表 `table` 与目标数据表 `table2` 进行合并。

![配置合并数据表组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeDataTable2020122502.png)
