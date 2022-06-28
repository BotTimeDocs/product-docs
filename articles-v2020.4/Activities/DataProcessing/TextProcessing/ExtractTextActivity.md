# 提取文本

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ExtractText.mp4"></video>

## 概述

支持提取指定文本内容中符合条件（正则表达式）的第一个结果，源文本内容不变。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **提取规则** ：点击“设置提取规则”后在弹窗中指定提取的规则
- **源文本** ：欲被提取的源文本数据。仅支持字符串变量和字符串

### 输出

- **提取结果** ：执行文本提取规则后提取的数据结果。仅支持字符串变量

## 使用示例

**此流程执行逻辑**：将源文本`"云扩RPA13812345678RPA"`中的手机号提取出来，保存至`result`变量中。

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010402.png)
