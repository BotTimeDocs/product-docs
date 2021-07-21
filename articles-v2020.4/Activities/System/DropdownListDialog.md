# 下拉选择框

## 视频示例

## 概述

提供人机交互界面，弹框形式展现并且带有下拉选择框，在界面选择动态填充的值并输出

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **默认索引** ：下拉选项的默认索引值。仅支持Int变量和数值

### 输入

- **标题** ：下拉选择框的标题。仅支持字符串变量和字符串
- **描述**：对该下拉选择框的一些说明
- **下拉选项** ：动态填充的下拉选项。仅支持String[]变量和String数组

### 输出

- **选中项** ：将选择的项存储在此变量。仅支持字符串变量和字符串

## 使用示例

1. 拖入**获取文件/文件夹列表**组件到设计面板，双击进入组件内部，设置参数。
<br/> 设置获取的文件路径参数，如"E:\shirley"；
<br/> 设置列表输出变量，如"files"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-1.png)

2. 拖入**下拉选择框**组件到设计面板，双击进入组件内部。
<br/> 设置下拉选择框的标题，如"E盘shirley目录下的文件"；
<br/> 下拉选项值为获取文件/文件夹列表组件输出的文件列表"files"；
<br/> 设置变量“value”为输出的选中项：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-2.png)

3. 拖入**写入日志**组件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-3.png)

4. 运行流程，选择下拉框的值“E:\shirley\hello.txt”，并点击“确认”按钮：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-4.png)

5. 查看控制台的输出，输出用户选择的下拉框选择的值，“E:\shirley\hello.txt”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-5.png)
