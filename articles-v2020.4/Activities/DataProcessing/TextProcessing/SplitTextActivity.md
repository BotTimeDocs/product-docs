# 分割文本

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SplitText.mp4"></video>

## 概述

根据指定的分割符分割文本。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **分隔符**：分隔原文本内容的分隔符号（该分隔符号包含在原文本中），可接变量。
- **原文本**：原始需要被分割的文本内容。

### 输出

- **分割结果**：分割的结果，仅可接变量。

### 可选项

- **移除空字符**：选择是否移除分隔后的空白项。

## 使用示例

**此流程执行逻辑**：将字符串`"123.56"`以`"."`为分隔符分割文本，分割后的文本存储至变量`S`中。

![配置属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/splittext20210104.png)
