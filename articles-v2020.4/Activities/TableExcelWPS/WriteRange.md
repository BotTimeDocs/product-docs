# 写入区域

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/WriteArea.mp4"> </video>

## 概述

将 Excel 工作表中的数据写入至同一个或不同 Excel 工作表的指定区域。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **工作表** ：写入数据表数据的目标工作表。若指定工作表不存在则自动新建。
- **起始单元格** ：数据表数据开始写入的单元格地址。若为单个单元格地址，则从指定单元格为起始写入数据表，如，`"A1"`；若为单元格区域，则只填充数据到指定区域，`"A1：C3"`。

### 输入

- **数据表** ：写入工作表内的数据表数据。可传入&quot; 读取区域&quot; 的输出变量，实现复制粘贴效果。

## 使用示例

**此流程执行逻辑**：读取 Excel 的 "sheet1" 中的“A1：D3”区域的内容，写入至 "sheet2" 中的“A1：D3”区域中。

![配置写入区域组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadRange2.png)

## 常见问题

1. **Q：如何在 Excel 中将两张表的内容，整合到第三张表中？**

    **A：** 可先读取前两张表的数据，一起写到第三个表。若前两张表结构一样，可使用 [合并数据表](../DataProcessing/DataTable//MergeDataTable.md)。
