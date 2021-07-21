# 获取单元格背景色

## 视频示例

## 概述

提取指定单元格的背景色，并返回十六进制值。同时可使用返回值作为&quot; 设置单元格背景色&quot; 的输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：目标单元格所属工作表。仅支持字符串变量和字符串
- **单元格** ：提取背景色的目标单元格，不支持单元格区域（填入区域时将无法执行）。仅支持字符串变量和字符串

### 输出

- **颜色** ：将指定单元格背景色存储在此变量。仅支持字符串变量和字符串

## 使用示例

1. 新建一个 Excel 文件，并在 Sheet1 的单元格 C7 和 D7 中分别设置背景色为黄色和黑色:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps33.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 2 个 **获取单元格背景色** 组件，分别填写工作表和单元格位置，以及输出的颜色的变量:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps34.png)

4. 拖入 **写入日志** 组件，来显示读取单元格颜色的内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps35.png)

5. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps36.png)