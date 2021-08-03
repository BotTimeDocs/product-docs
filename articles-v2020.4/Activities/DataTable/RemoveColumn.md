# 移除列

## 视频示例

## 概述

删除指定数据表的指定列，并自动保存同步其数据至指定数据表。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将移除此表的指定列。
- **数据表列** ：移除数据表中的数据表列对象。和&quot;列名，列索引&quot;属性互斥，只能且必需填入一项。
- **列名** ：移除数据表中的指定列的列名。和&quot;数据表列，列索引&quot;属性互斥，只能且必需填入一项。
- **列索引** ：移除数据表中指定列的列索引。和&quot;数据表列，列名&quot;属性互斥，只能且必需填入一项。

## 使用示例

**前置必要组件**：[搭建数据表](../DataTable/BuildDataTable.md)

**此流程执行逻辑**：将已搭建的数据表`table`中的`"姓名"`列移除。

![配置移除列组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveColumn20201228.png)
