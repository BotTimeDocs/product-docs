# 设置数据行的值

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SetDataRowsValue.mp4"></video>

## 概述

设置已有 **非空** 数据表的指定数据行所在单元格的值。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **列索引**：被设置的单元格所在列的位置，默认第一列为 0。
- **数据行**：已搭建的非空数据表所在数据行。如，数据表的第一行 `dt.Rows[0]`。
- **值**：设置由数据行和列索引组合构成的单元格的值。

## 使用示例

**前置必要组件**：[搭建数据表](../DataTable/BuildDataTable.md)

**此流程执行逻辑**：向已创建的 `dt` 数据表的第 2 行第 3 列所在的单元格中添加一个值为 `56`。

![设置数据行的值](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingdatarow20210806.png)
