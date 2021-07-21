# 获取文本索引

## 视频示例

## 概述

获取指定文本所在源文本的索引

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **源文本** ：输入源文本数据。仅支持字符串变量和字符串
- **被检索文本** ：输入被检索的文本数据。仅支持字符串变量和字符串

### 输出

- **索引** ：被检索的文本索引，仅支持Int变量。

## 使用示例

1. 拖入**获取文本索引组件**，创建变量并填入变量，所下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010501.png)

2. 拖入其它组件，例：拖入**写入日志**组件，将获取到的文本索引输出到日志，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010502.png)

3. 点击运行，成功获取到文本索引，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010503.png)