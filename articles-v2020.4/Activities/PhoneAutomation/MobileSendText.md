# 发送文本

## 视频示例

## 概述

将文本内容发送至光标所在处。

>**说明：**
>
> - 该组件仅能放置于**连接设备**组件内，且操作自动绑定至外层设备。
> - 在该组件前建议放置点击等组件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **输入后回车**：输入文本后是否回车。选择“是”时，输入文本后自带一个回车符；选择“否”时，输入文本后无附加回车符。

### 输入

- **文本**：输入待发送的文本内容。

## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**点击**组件。
3. 单击**点击**组件中的“指定元素”链接，指定需要输入文本内容的地方。

    ![指定输入内容地址](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingsendtext20201223.png)

4. 在**点击**组件下方，拖入一个**发送文本**组件。
5. 在**发送文本**组件中的文本框中输入一段需发送的文本内容，如，"Hello!"。

    ![发送文本内容](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sendtextflow20201223.png)

6. 保存并运行流程，可看到需要发送的文本被发送至微信的发送框中，运行效果如下图所示。

    ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/showsendtext20201223.png)