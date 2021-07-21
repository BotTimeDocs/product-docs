# 设置单元格背景色

## 视频示例

## 概述

对指定单元格进行填充背景色(16 进制颜色码)操作。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **单元格** ：指定填充颜色的目标单元格，可填入单元格地址(如，"A1")或单元格区域（如，"A1：C10"）。此处不可为空，否则运行失败
- **工作表** ：指定目标单元格所属工作表名称。仅支持字符串变量和字符串

### 输出

- **颜色** ：指定填充色(16 进制颜色码)；支持手动输入和从拾色器选择；仅支持字符串变量和字符串

## 使用示例

1. 拖入 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入 **设置单元格背景色** 组件至项目流程中，填写 sheet 名称“sheet1”，填写单元格名称“A1”或者是区域“A1：D3”，点击组件右下角颜色选择器，选择一个颜色：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetCellBackColor1.png)

4. 组件颜色选择器点击高级 tab，拖动或者填写颜色编码：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetCellBackColor2.png)

5. 组件属性面板点击颜色，直接输入颜色编码：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetCellBackColor3.png)

6. 点击运行，运行成功后，打开 excel，对应的单元格或者区域颜色设置成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetCellBackColor4.png)
