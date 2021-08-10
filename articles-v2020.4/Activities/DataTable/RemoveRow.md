# 移除行

## 视频示例

## 概述

删除指定数据表的指定行，并自动保存同步其数据至指定数据表

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将移除此表的指定行
- **数据表行** ：移除数据表中的数据表行对象。和&quot; 行索引&quot; 属性两者互斥，只能且必需填入一项
- **行索引** ：移除数据表中行的行索引。和&quot; 数据表行&quot; 属性两者互斥，只能且必需填入一项。仅支持整型变量和整型

## 使用示例

**前置必要组件**：已有一个已搭建的数据表，可参见 [搭建数据表](../DataTable/BuildDataTable.md)。

**此流程执行逻辑**：将已搭建的数据表 `table` 中的第三行数据移除。

![配置移除行组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveRow20201228.png)
