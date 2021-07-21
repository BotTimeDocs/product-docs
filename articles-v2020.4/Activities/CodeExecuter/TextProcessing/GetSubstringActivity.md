# 截取文本

## 视频示例

## 概述

支持截取指定文本内容中符合条件(开始位置和结束位置)的第一个结果

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **源文本** ：欲被截取的源文本数据。仅支持字符串变量和字符串
- **开始位置** ：指定截取的开始位置，若为空或0则从第一个字符开始。仅支持Int变量或整型数值
- **结束位置** ：指定截取的结束位置，若为空或0则从第一个字符开始。仅支持Int变量或整型数值

### 输出

- **截取结果** ：截取的文本数据。仅支持字符串变量

## 使用示例

1. 拖动**截取文本**组件至项目流程中，创建组件所需变量，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetSubstringActivity2021010501.png)

2. 拖入其它组件，例：拖入**写入日志**组件，填入输出日志内容，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetSubstringActivity2021010502.png)

3. 点击运行，流程运行成功，成功将文本截取出来，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetSubstringActivity2021010503.png)