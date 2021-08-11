# 插入工作表

## 视频示例

## 概述

在工作簿内插入指定的工作表。

>**说明：**：
>
>此组件仅可在“打开/新建”组件中使用。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **插入模式** ：包括两种模式：新建工作表，复制工作表。

    >**说明：**
    >
    >- 新建工作表模式指将在工作簿中创建一个新的工作表并插入到指定位置。
    >- 复制工作表模式指将在工作簿中复制已有工作表副本并插入到指定位置。

- **插入位置** ：指定插入工作表的位置。例如“1”，即插入工作表的位置为第一个。当为空时，默认插入到最后；超过最大位置，则默认插入到最后。
- **新工作表名称** ：欲插入的新工作表名。
- **源工作表名** ：欲复制的工作表名。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：在Excel工作簿中的指定工作表位置插入
新的工作表“sheetNew”并复制工作表“Sheet1”的内容填充。

![配置插入工作表组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertWorksheets1.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertWorksheets2.png)
