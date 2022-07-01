# 滑动屏幕

## 视频示例

## 概述

模拟人工进行尝手机屏幕效果。

> **说明：**
>
> 该组件仅能放置于 **连接设备** 组件内，且操作自动绑定至外层设备。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **[选择器](../Appendix/Selector.md)**：用于指示要点击的目标位置。可通过点击 **指定元素** 自动生成。仅支持字符串变量和字符串。

## 使用示例

**前置必要组件**：[连接设备](../PhoneAutomation/MobileConnect.md)

**此流程执行逻辑**：实现手机屏幕左滑或右滑的效果。

![滑动屏幕](https://docimages.blob.core.chinacloudapi.cn/images/Activities/swipescreen20201223.png)

## 常见问题

1. **Q：组件提示错误信息：“case 运行失败”。**

    **A：** 单独执行加一个 2 秒或 3 秒的前延时。
