# 执行命令行

## 视频示例

## 概述

执行 CMD 命令行，并提供返回值。如，使用命令行实现 60 秒后定时关机： “shutdown -s -t 60”。

> **说明：**
>
> 此组件也支持对 Python 文件的操作，例如：在“命令行”属性中填写“Python Test.py arg1 arg2”, 其中“arg1”和“arg2”为参数。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作目录** ：指定运行命令的工作目录
- **命令行** ：执行该命令行。仅支持字符串变量和字符串

### 输出

- **输出**：将命令行执行后的结果存储到此变量

## 使用示例

**此流程执行逻辑**：执行 cmd 命令，并将执行结果保存至“result”变量中。

![配置执行命令行组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-2.png)
