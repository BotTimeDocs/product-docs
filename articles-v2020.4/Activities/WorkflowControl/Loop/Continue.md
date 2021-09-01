# 继续循环

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/KeepLooping.mp4"></video>

## 概述

跳出当前次循环，执行下一次循环。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

## 使用示例

**此流程执行逻辑**：在**循环操作（For Each）** 组件内，拖入**流程决策**组件并输入判断条件 item == 1，当判断条件为真时跳出当次循环并开始执行下一次循环；当判断条件为假时将当前值作为日志文本输出。

![配置继续循环组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/continue-4.png)
