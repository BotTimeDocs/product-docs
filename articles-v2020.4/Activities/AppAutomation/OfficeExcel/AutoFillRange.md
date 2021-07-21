# 自动填充

## 视频示例

## 概述

从源单元格区域自动填充数据到目标区域。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：执行填充操作的目标工作表。若指定工作表不存在则报错。仅支持字符串变量和字符串
- **填充区域** ：欲将源数据自动填充的目标区域
- **源区域** ：进行填充操作的源单元格区域

## 使用示例

1. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖拽 **自动填充** 到 **打开/新建** 组件中，填写 sheet 名称，填写源区域 "A1: C3"。填充区域，请注意支持横向填充 "A1: I3"，或者是纵向填充 "A1: C9", 必须包含源区域，不支持同时横向和纵向填充：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AutoFillRange1.png)

4. 点击运行，运行成功。打开 Excel，横向填充成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AutoFillRange2.png)