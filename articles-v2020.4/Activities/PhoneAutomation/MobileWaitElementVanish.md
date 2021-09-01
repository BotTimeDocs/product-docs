# 等待元素消失

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/WaitElementDisapper.mp4"></video>

## 视频示例

## 概述

等待指定元素的消失，支持图像识别和指定元素。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **结果**：将此组件执行的成功与否的结果存储在此变量。当指定目标出现时，存储的值为True。

### 目标

- **[选择器](../Appendix/Selector.md)**：要获取的特定UI元素。可通过点击指定元素自动生成。
- **匹配超时(毫秒)**：限定查找目标元素时间，超出指定时间后将不再等待，1000ms =1s。

## 使用示例

**前置必要组件**：[连接设备](./MobileConnect.md)

**此流程执行逻辑**：指定等待消失的元素，将 **等待元素消失** 组件返回的结果输出至“输出面板”中。

![配置等待元素消失](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingwaitelementvanish20201224.png)
