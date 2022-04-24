# 消费任务

## 视频示例

## 概述

指定云扩 RPA 控制台（企业版）的“RPA 中心 > 任务队列”中的消息并在流程中处理。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **部门**：单击组件中的“设置参数”，在弹框中选择该登录用户所在控制台中的公司下的“部门”。
- **任务队列**：从部门下选择对应的任务队列名称。
- **处理完成后**：选择消息被获取处理后的行为。
- **无消息时**：指定当流程运行到当前组件时若队列中无消息的后续行为。

### 输出

- **消息**：输出从任务队列中获取的消息。仅支持变量。