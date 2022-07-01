# 追加文本

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/AppendText.mp4"></video>

## 概述

将指定文本追加至原文本最后面。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **源文本**：输入原始文本内容。
- **追加文本**：输入希望追加的文本内容。

### 输出

- **追加结果**：追加的结果，仅可接变量。

### 可选项

- **换行追加**：是否需要换行追加。勾选后则将新文本在原文本换行后进行追加，否则不换行追加。

## 使用示例

**此流程执行逻辑**：向源文本 `Hello` 中追加文本 ` World!`，最终将追加结果保存至变量 `S` 中。

![追加文本](https://docimages.blob.core.chinacloudapi.cn/images/Activities/appendtext20210111.jpg)
