# 移除键值对

## 视频示例

## 概述

从已初始化的字典中移除所指定的键值对。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **键**：移除的字典中指定的键值对。
- **字典**：在变量面板中定义的字典对象，仅可接变量。

### 输出

- **结果**：是否将字典中的指定移除的键值对移除成功，仅可接变量。

## 使用示例

**前置必要条件**：已有一个已添加键值对的字典，可参见 [添加键值对](../Dictionary/AddDictionaryActivity.md)

**此流程执行逻辑**：将已添加键值对的字典 `D` 中的键值对(`key3`、`value3`)移除，返回结果存储至变量 `S` 中。

![配置移除键值对组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/removekeyvalue20210112.png)
