# 是否包含键/值

## 视频示例

## 概述

判断在变量面板中定义的字典对象中是否包含键（key）及对应的值（value）。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **检测内容**：与“键/值”属性对应的需要检测的参数内容。
- **键/值** ：需要判断字典中是否包含参数 key 和参数 Value 的值。
- **字典**：在变量面板中定义的字典对象，仅可接变量。

### 输出

- **结果**：是否包含“键/值”的结果，仅可接变量。

## 使用示例

**前置必要组件**：[初始化字典](../Dictionary/InitializeDictionaryActivity.md)
**此流程执行逻辑**：判断已有的字典`D`中是否包含键`"key3"`，返回结果存储至变量`R`中。

![配置是否包含键/值组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/containtskeyvalue20210111.png)
