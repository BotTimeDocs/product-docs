# 日期和时间选择框

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/DatetimeSelectionBox.mp4"></video>

## 概述

流程运行时弹窗让用户选择日期和时间并输出。
> **说明：**
>
> 运行时窗口中默认显示为当前日期和时间。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **标题**：（非必填）自定义 **日期和时间选择框** 组件运行时的标题。
- **描述**：（非必填）自定义 **日期和时间选择框** 组件运行时的描述信息。

### 输出

- **选择的时间** ：输出用户在弹窗中指定的日期和时间。

## 使用示例

**此流程执行逻辑**：弹框让用户选择指定的日期和时间，并在“输出面板”中输出。

![配置日期和时间选择框组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/timePicker-2.png)

**执行结果**：
![选择指定的日期和时间](https://docimages.blob.core.chinacloudapi.cn/images/Activities/timePicker-4.png)

## 常见问题

1. **Q：在点击图标会出现的日历框中选择时间，如何定位到每月的26号？**

    **A：** 需要根据具体的日期控件分析。由于系统不同，日期框的实现也不一样，可以直接设置的日期框较简单，需要点击选择的日期框，要看日期的控件属性。
