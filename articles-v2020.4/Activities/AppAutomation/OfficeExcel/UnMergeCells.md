# 取消单元格合并

## 视频示例

## 概述

对指定单元格区域已合并的单元格进行拆分，拆分后的值显示在左上角第一个单元格内。

>**说明：**
>
>该组件需在 Office Excel 的 **打开/新建** 组件内进行使用。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：指定欲进行取消合并单元格操作所属工作表名称。
- **单元格** ：指定欲进行取消合并的单元格区域。

### 输出

- **值**：取消合并后单元格内显示的值。

## 使用示例

**前置必要组件**：[打开/新建](../OfficeExcel/OpenExcel.md)

**此流程执行逻辑**：取消合并指定工作表“Sheet1”中待取消合并的数据所在单元格“A14”。

![配置取消单元格合并组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SettingUnMergeCells20210722.png)
