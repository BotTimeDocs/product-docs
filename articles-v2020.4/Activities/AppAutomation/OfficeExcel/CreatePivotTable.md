# 创建透视表

## 视频示例

## 概述

此组件可实现在 Excel 中创建透视表

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标位置

- **目标工作表** ：输入创建的透视表所在目标工作表。仅支持字符串变量和字符串
- **目标区域** ：输入创建的透视表所在目标区域。仅支持字符串变量和字符串
- **透视表名称** ：输入创建的透视表名称。仅支持字符串变量和字符串

  > **说明：**
  >
  > 在“创建透视表”弹窗中，需指定透视表字段，需输入字母列号，例如：在“筛选”中输入“A, B”，则创建的透视表以 A 列和 B 列作为筛选列。

### 数据源

- **源表名** ：输入数据源中的表名（和“源区域”属性互斥，二选一）。仅支持字符串变量和字符串
- **源工作表** ：输入数据源所属工作表。仅支持字符串变量和字符串
- **源区域** ：输入数据源中的区域（和“源表名”属性互斥，二选一）。仅支持字符串变量和字符串

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **创建透视表** 组件到 **打开/新建** 组件中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable2.png)

5. 点击创建透视表向导，填写源工作表“sheet1”，区域 "A1: D11"；填写目标工作表“sheet1”，目标区域 "F1: H11"，透视表名称 "销售统计"；填写透视表字段如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable3.png)

6. 运行成功后，在目标区域生成如下透视表：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable4.png)
