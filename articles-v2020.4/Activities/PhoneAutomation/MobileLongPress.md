# 长按屏幕

## 视频示例

## 概述

模拟人工进行长按手机屏幕指定元素效果。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **[选择器](../Appendix/Selector.md)**：用于指示要点击的目标位置。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串。

## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**长按屏幕**组件。
3. 单击**长按屏幕**组件中的**指定元素**链接，进入**移动设备管理器**界面指定元素，如下图所示。

   ![指定元素](https://docimages.blob.core.chinacloudapi.cn/images/Activities/locatelongpress20201223.png)

4. 保存并运行流程，可看到长按“京东金融”应用的效果，如下图所示。

   ![长按效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/longpress20201223.png)