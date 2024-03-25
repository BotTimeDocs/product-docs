# 并行

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Parallel.mp4"></video>

## 概述

同时执行此组件内所包含的纵向序列下的组件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **结束条件**：设置结束执行的条件。

## 使用示例

**此流程执行逻辑**：左侧流程延迟时间段内会运行右侧流程。

![配置并行组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pallel-2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pallel-3.png)

> 如需在主流程执行同时并行执行流程，可参考：[并行处理流程](https://academy.encoo.com/wiki/Studio/process/developProject/TypeOfWorkflow/Parallel.md)
