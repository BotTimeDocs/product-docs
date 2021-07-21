# 获取单元格背景色

## 视频示例

## 概述

提取指定单元格的背景色，并返回十六进制值。同时可使用返回值作为&quot; 设置单元格背景色&quot; 的输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：指定目标单元格所属工作表名称。仅支持字符串变量和字符串
- **单元格** ：提取背景色的目标单元格，不支持单元格区域（填入区域时将无法执行）。仅支持字符串变量和字符串

### 输出

- **颜色** ：输出指定单元格背景色，例如 "#FFFFFF"。仅支持字符串变量和字符串

## 使用示例

1. 拖入 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入 **获取单元格背景色** 组件至项目流程中，填写 sheet 名称“sheet1”，填写单元格名称“A1”，新建变量 "color" 类型为 String，属性面板颜色配置变量 "color"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetCellBackColor1.png)

4. 点击运行，运行成功后，打开 excel，对应的单元格或者区域颜色设置成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetCellBackColor2.png)
