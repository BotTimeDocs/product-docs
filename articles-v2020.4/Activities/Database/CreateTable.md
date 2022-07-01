# 创建表

## 视频示例

## 概述

在已连接的数据库内，创建数据表。

> **说明：**
>
> 该组件仅可作用于 **连接数据库** 或 **执行事务** 组件内。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **表名**：欲创建的表的名称。
- **数据表**：根据此数据表结构创建表并将已有数据插入到表中。一般使用**搭建数据表**的输出作为该数据表的输入。

### 可选项

- **超时**：超时时间（时分秒），默认超时时间：00:00:30，可接变量。
- **如果存在忽略**：如果数据库已存在相同名称的表，则忽略此次操作。
- **主键列名**：主键的列名。

## 使用示例

**前置必要组件**：[搭建数据表](../DataProcessing/DataTable/BuildDataTable.md)

**此流程执行逻辑**：根据已有的数据表结构`outtable`在数据库`test`中创建表`testdemo`。

![创建表](https://docimages.blob.core.chinacloudapi.cn/images/Activities/createtable20210924.png)
