# 延迟

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Delay.mp4"></video>

## 概述

在下一个组件执行前的等待时间，当指定的等待时间过后，开始执行此组件后的流程。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **等待时间** ：设置延迟时间，格式：时:分:秒。

## 使用示例

**此流程执行逻辑**：在执行完“打开浏览器”组件后，等待5秒后，再执行“输入文本”组件。

![配置延迟组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/delay-2.png)
