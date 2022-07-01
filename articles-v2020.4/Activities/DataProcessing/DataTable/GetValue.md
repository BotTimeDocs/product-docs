# 获取单元格的值

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetCellValue.mp4"></video>

## 概述

将数据表内指定单元格内值的存储到输出值变量。

>**说明：**
>
>结合**筛选**组件一起使用，当输出的是一个一行一列的数据表时，此组件输入属性坐标为（1，1）时，可实现取数据表中特定坐标值的效果，变相实现查找（例姓名为张三的成绩）。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：读取此数据表中的值。
- **行索引** ：指定要获取数据表值的行索引。
- **列索引** ：指定要获取数据表值的列索引。

### 输出

- **值** ：将获取到数据表内的单元格值存储到此变量。

## 使用示例

**前置必要组件**：[搭建数据表](../../DataProcessing/DataTable/BuildDataTable.md)

**此流程执行逻辑**：从已搭建的数据表`table`中获取第二行第二列单元格的值，存放至`cellvalue`变量中。

![配置获取单元格的值组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetValueDataTable20201229.png)
