# 替换文本

## 视频示例

## 概述

支持将文本内容中符合条件的第一个内容替换为期望值

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **源文本** ：欲被替换的源文本数据。仅支持字符串变量和字符串
- **查找内容** ：指定欲被替换的内容。仅支持字符串变量和字符串
- **新内容** ：指定欲替换成的内容。仅支持字符串变量和字符串

### 输出

- **替换结果** ：替换后的结果。仅支持字符串变量

## 使用示例

1. 拖入**替换文本**组件至项目流程中

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReplaceTextActivity2021010501.png)

2. 创建变量，并将其填入对应输入框中，如下图所示：

![Image Text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReplaceTextActivity2021010502.png)

3. 拖入其它组件至流程中，例：拖入写入日志组件，如下图所示：

![Image Text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReplaceTextActivity2021010503.png)

4. 点击运行，流程运行成功，如下图：

![Image Text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReplaceTextActivity2021010504.png)