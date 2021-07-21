# 清空文本

## 视频示例

## 概述

清空指定输入框内的文本。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **[选择器](../../Activities/Appendix/Selector.md)**：要获取的特定UI元素。可通过点击指定元素自动生成，仅支持字符串变量和字符串。

## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**清空文本**组件。
3. 单击**清空文本**组件中的**指定元素**链接，在移动设备管理器界面指定需要清空的文本，如下图所示。
   ![清空文本](https://docimages.blob.core.chinacloudapi.cn/images/Activities/locatecleartext20201224.png)

4. 保存并运行流程，可看到屏幕上文本框中的内容被清空的效果。