# 删除表

## 视频示例

## 概述

删除已连接的数据库内已创建的数据表。

> **说明：**
>
> 该组件仅可作用于 **连接数据库** 或 **执行事务** 组件内。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **表名**：欲删除的表名称。

### 可选项

- **超时**：超时时间（时分秒），默认超时时间：00: 00: 30，可接变量。

## 使用示例

**前置必要条件**：数据库中已有需要删除的数据表，可通过 [创建表](./CreateTable.md) 组件创建表。

**此流程执行逻辑**：删除数据库中已创建的数据表 `testdemo`。

![删除表](https://docimages.blob.core.chinacloudapi.cn/images/Activities/deletetable20210924.png)
