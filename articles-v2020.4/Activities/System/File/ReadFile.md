# 读取文件

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ReadFile.mp4"></video>

## 概述

读取指定文件内容并可将其数据存储在变量中。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件路径** ：读取此路径文件的内容。支持相对和绝对路径。可在组件面板点击弹出对话框，选择目标文件；亦支持手动输入路径，若路径不存在，则运行失败。

### 输出

- **文件内容**：将目标文件内容存储到此变量。

### 可选项

- **编码方式** ：文件的编码方式。可以在 [此处](../../Appendix/Encoding.md?_v=v2020.4) 找到每个字符编码的完整代码列表。要指定要使用的编码类型，请使用“名称”字段中的值。如果未指定编码类型，则活动将搜索文件的字节顺序标记以检测编码。如果未检测到字节顺序标记，则默认选择系统ANSI代码页。

## 使用示例

**此流程执行逻辑**：读取D盘下的“新建文本文档.txt”文件中的内容，并输出至“输出面板”中。

![配置读取文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/readFile-2.png)

## 常见问题

1. **Q：如何解决读取文件乱码问题？**

    **A：** 可尝试将设置文件中字符`UTF-8`换为`GBK`编码。