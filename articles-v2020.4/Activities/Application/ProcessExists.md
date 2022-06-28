# 进程是否存在

## 视频示例

## 概述

根据指定的进程名，判断本地电脑上的进程名是否存在。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **进程名称**：进程的名称。

### 输出

- **结果**：将返回的结果存储至此变量，结果分为 True 和 False。

## 使用示例

**此流程执行逻辑**：检查本地电脑上的 `"RuntimeBroker"` 进程是否存在，若存在返回 True，否则返回 False。

![配置进程是否存在组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/processexists20210927.png)
