# 遍历行

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/IterateOverRows.mp4"></video>

## 概述

遍历指定数据表中的每一行，同时可返回当前行索引。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表**：取此表执行遍历操作。

### 输出

- **当前行索引** ：将当前正在被遍历的行索引存储在此变量。仅支持整型变量和整型

## 使用示例

**前置必要条件**：已有一个已搭建的数据表，可参见 [搭建数据表](../../DataProcessing/DataTable/BuildDataTable.md)。

**此流程执行逻辑**：遍历检查数据表 `table` 的每行的行值和姓名值。

![配置遍历行组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ForEachRow20201228.png)
