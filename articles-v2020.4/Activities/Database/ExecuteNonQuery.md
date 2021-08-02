# 执行语句（Non Query）

## 视频示例

## 概述

执行指定的Non Query语句，例如UPDATE, INSERT, DELETE，并返回语句执行后受影响的作用行数。若执行其他非Non Query 语句，返回-1。

>**说明**：
>
>需在“连接数据库”和“执行事务”内使用，无需二次配置连接。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **Sql语句** ：要执行的Non Query语句。

### 输出

- **作用行数** ：将语句执行后受影响的作用行数存储到此变量。

### 可选项

- **超时**：超时时间（时分秒），默认超时时间：00:00:30，可接变量。

## 使用示例

**前置必要组件**：[连接数据库](../Database/ConnectDatabase.md)

**此流程执行逻辑**：更新数据库中`test.testconnect`数据表中`C`列的数据。

![配置执行语句组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db7.png)
