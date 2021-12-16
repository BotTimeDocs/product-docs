# 写入单元格

## 视频示例

## 概述

写入数据到指定单元格。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **单元格** ：写入数据的目标单元格地址。可输入单元格或区域，当输入区域时，则在指定区域每一个单元格内输入相同数据。
- **工作表** ：写入数据的目标工作表。若指定工作表不存在则自动新建。
- **数据** ：写入单元格内的数据。可传入&quot; 读取单元格&quot; 的输出变量，实现复制粘贴效果，同时保持复制源的数据格式。

## 使用示例

**前置必要组件**：[打开/新建](../WPSExcel/OpenExcel.md)

**此流程执行逻辑**：在`wps.xlsx`工作簿的`Sheet1`工作表的`A1`单元格中写入`"测试写入单元格"`内容。

![配置写入单元格组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps44.png)

## 常见问题

1. **Q：“写入单元格”组件，报错“[错误]活动仅在WPS表格打开/新建中有效”。**

    **A：** “写入单元格”组件需在“打开/新建”组件内部。

    ![写入单元格组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/writecell20210825.png)

1. **Q：Office写入完单元格后能否不要自动关闭？即新建/打开后不自动关闭。**

    **A：** 设计就是需要自动关闭的，因为场景可能有很多个Excel文件处理。
