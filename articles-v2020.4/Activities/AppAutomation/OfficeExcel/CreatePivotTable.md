# 创建透视表

## 视频示例

<video controls height='450px' width='800px' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/CreatePivotTable.mp4"></video>

## 概述

实现在 Excel 中创建透视表。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标位置

- **目标工作表** ：输入创建的透视表所在目标工作表。
- **目标区域** ：输入创建的透视表所在目标区域。
- **透视表名称** ：输入创建的透视表名称。

  > **说明：**
  >
  > 在“创建透视表”弹窗中，需指定透视表字段，需输入字母列号，例如：在“筛选”中输入“A, B”，则创建的透视表以 A 列和 B 列作为筛选列。

### 数据源

- **源表名** ：输入数据源中的表名（和“源区域”属性互斥，二选一）。
- **源工作表** ：输入数据源所属工作表。
- **源区域** ：输入数据源中的区域（和“源表名”属性互斥，二选一）。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)
**此流程执行逻辑**：创建一个销售统计表，将“Sheet1”工作表的“A1：D11”区域的数据筛选后展示于“F1: H11”区域中。

![配置创建透视表组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable3.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable4.png)
