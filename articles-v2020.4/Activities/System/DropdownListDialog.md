# 下拉选择框

## 视频示例

## 概述

提供人机交互界面，弹框形式展现并且带有下拉选择框，在界面选择动态填充的值并输出。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **标题** ：下拉选择框的标题。
- **描述**：对该下拉选择框的一些说明
- **下拉选项** ：动态填充的下拉选项。

### 输出

- **选中项** ：将选择的项存储在此变量。

### 可选项

- **默认索引** ：下拉选项的默认索引值。

## 使用示例

**前置必要组件**：[获取文件/文件夹列表](../System/File/GetFileOrFolderList.md)

**此流程执行逻辑**：下拉选择框中的选项值为获取文件/文件夹列表组件输出的文件列表“files”，将选中的下拉选择框中的值，输出至“输出面板”中。

![配置下拉选择框组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-4.png)
