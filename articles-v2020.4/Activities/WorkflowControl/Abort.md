# 终止流程

## 视频示例

## 概述

当执行到此组件时立即结束当前流程，不再执行后续流程。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

## 使用示例

1. 拖入**循环操作（While）** 组件，创建变量count并设置循环条件 count <= 100：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-1.png)

2. 设置两个变量，分别为workEndDT & workStartDT，设置变量类型TimeSpan，默认值分别为`DateTime.Parse("7:30").TimeOfDay` & `DateTime.Parse("20:30").TimeOfDay`; 拖入**流程决策**组件，设置判断条件: `DateTime.Now.TimeOfDay > workEndDT && DateTime.Now.TimeOfDay < workStartDT`:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-2.png)

3. 如果判断条件为真，则用**终止流程**组件终止流程；如果判断条件为假，则用**赋值**组件进行变量递增，循环继续：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-3.png)

4. 点击运行流程，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-4.png)