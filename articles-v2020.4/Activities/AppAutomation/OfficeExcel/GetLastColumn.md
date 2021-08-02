# 获取末列号

## 视频示例

## 概述

获取工作表或指定行有数据区域的最后一列列号。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：获取末列号操作所属工作表。
- **行** ：获取末列号的所属行索引（例：1，即获取第一行的末列号）。当此项为空时，取整表数据区域最后一列列号。

### 输出

- **末列号(数字)** ：输出获取的数字末列号。
- **末列号(字母)** ：输出获取的字母末列号。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)
**此流程执行逻辑**：获取“Sheet1”工作表第一行有数据区域的最后一列列号。

![配置获取末列号组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLastColumn1.png)
