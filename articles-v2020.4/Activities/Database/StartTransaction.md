# 执行事务（Transaction）

## 视频示例

## 概述

其内可放置其他数据库组件来实现执行事务功能，这些操作要么全部执行要么全部不执行。

>**说明**：
>
>- 需在“连接数据库”和“执行事务”内使用，无需二次配置连接。
>- 如果是对表结构删除或更新，目前除MS SQL外，其他数据库则无法实现回滚，依赖于各数据库本身功能。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

## 使用示例

**前置必要组件**：[连接数据库](../Database/ConnectDatabase.md)

**此流程执行逻辑**：在执行事务中，使用**执行语句**组件更新数据库中`test.testconnect`数据表中`C`列的数据。

![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db11.png)
