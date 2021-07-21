# 查找

## 视频示例

## 概述

在特定单元格区域内查找给定值，并返回第一个查找到的单元格地址。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **单元格匹配**：精确完整匹配单元格内容。
- **匹配大小写**：匹配查找内容大小写。

### 输入

- **查找内容** ：取此值进行查找。仅支持字符串变量和字符串
- **工作表** ：执行查找操作的目标工作表。仅支持字符串变量和字符串
- **区域** ：查找操作的目标单元格区域。为空时，默认查找全表

### 输出

- **单元格地址** ：将查找到的第一个单元格地址存储在此变量。仅支持字符串变量和字符串

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Search1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **排序** 和 **写入日志** 到 **打开/新建** 组件中，填写 sheet 名称 "sheet2"，填写搜索区域，填写搜索的关键字“100”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Search2.png)

5. 运行成功后，输出面板打印关键字所在的位置：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Search3.png)