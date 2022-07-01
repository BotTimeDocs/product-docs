# 写入文件

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/WriteFile.mp4"></video>

## 概述

将“写入内容”，覆盖写入到指定文件；若文件不存在，则新建。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件路径** ：将“写入内容”，覆盖写入到此文件。支持相对和绝对路径。可在组件面板点击弹出对话框，选择目标文件；亦支持手动输入路径，若路径不存在，则新建。
- **写入内容** ：写入目标文件的内容。

### 可选项

- **编码方式** ：文件的编码方式。可以在 [此处](../Appendix/Encoding.md?_v=v2020.4) 找到每个字符编码的完整代码列表。要指定要使用的编码类型，请使用“名称”字段中的值。如果未指定编码类型，则活动将搜索文件的字节顺序标记以检测编码。如果未检测到字节顺序标记，则默认选择系统 ANSI 代码页。

- **写入模式** ：选项：另起新行写入（默认）、文件末尾写入和覆盖原文写入。

## 使用示例

**此流程执行逻辑**：将指定的文件内容“Hello, World!”写入到 D 盘下的“material.xls”文件中。

![配置写入文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/writeFile-1.png)
