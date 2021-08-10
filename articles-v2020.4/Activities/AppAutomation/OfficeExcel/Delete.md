# 删除数据

## 视频示例

<video controls height='450px' width='800px' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/DeleteData.mp4"></video>

## 概述

对指定工作表进行删除操作。可实现删除单元格、整行、整列、区域、工作表。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **单元格** ：删除操作的目标单元格地址。若只需删除单个单元格内数据，则填充此项。
- **工作表** ：执行删除操作的目标工作表。
- **列** ：删除整列数据。若需删除整列数据，则填充此项（例：1，即删除第一列）
- **区域** ：删除操作的目标单元格区域。若需删除区域数据，则填充此项。
- **删除整表** ：勾选时，删除指定工作表。
- **行** ：删除整行数据。若需删除整行数据，则填充此项（例：1，即删除第一行）。

    > **注意：**
    >
    >上述“输入”属性中的六项，除“工作表”外，剩余五项必须五选一且互斥。

### 可选项

- **移动单元格** ：勾选时，删除数据同时将移动单元格，“移动模式”以用户选择为准；不勾选时，仅删除文本且不清空格式。
- **移动模式** ：当勾选&quot; 移动单元格&quot; 时，下拉此项选择单元格的移动模式，具体效果实现同 Office Excel。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：删除Sheet1工作表的第三行数据。

![配置删除数据组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Delete2.png)
