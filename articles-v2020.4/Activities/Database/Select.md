# 查询

## 视频示例

## 概述

对数据库执行查询操作并将结果返回到数据表。

>**说明**：
>
>需在“连接数据库”和“执行事务”内使用，无需二次配置连接。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **Sql语句**：要执行的查询语句。

### 输出

- **数据表** ：执行查询后得到的数据表存储到此变量。

### 可选项

- **超时**：超时时间（时分秒），默认超时时间：00:00:30，可接变量。

## 使用示例

**前置必要组件**：[连接数据库](../Database/ConnectDatabase.md)

**此流程执行逻辑**：查询数据库中`test.testconnect`数据表中的数据。

![配置查询组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db3.png)
