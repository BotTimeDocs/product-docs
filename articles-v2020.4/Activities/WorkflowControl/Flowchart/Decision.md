# 流程决策

## 视频示例

## 概述

根据是否满足指定条件，选择执行流程图中两个分支。

>**说明：**
>
>此组件只能在流程图中使用，效果类似“条件”组件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **Condition** ：流程决策的条件，支持Boolean类型的表达式。

### 杂项

- **False Label** ：当决策为False时的标签名称。
- **True Label** ：当决策为True时的标签名称。

## 使用示例

**前置可选组件**：等待元素出现

**此流程执行逻辑**：执行流程决策组件的True和False端的流程。

![流程决策](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decision-2.png)
