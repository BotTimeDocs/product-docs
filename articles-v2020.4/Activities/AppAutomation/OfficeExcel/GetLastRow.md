# 获取末行号

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetLastColumn.mp4"> </video>

## 概述

获取工作表或指定列有数据区域的最后一行行号。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：需要获取的末行号所属工作表。
- **列类型**：选择 Excel 中列的类型。
- **数字列号**：数字形式的列号，如，1、2、3 等。
- **字母列号**：字母形式的列号，如，A、B、C 等。

### 输出

- **末行号** ：将取到的末行号存储在此整型变量内。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：获取 Excel 工作表指定列的有数据的最后一行的行号。

![配置获取末行号组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLastRow1.png)
