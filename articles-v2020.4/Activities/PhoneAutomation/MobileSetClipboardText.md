# 设置剪贴板文本

## 视频示例

## 概述

将指定的字符串文本设置到手机剪贴板中。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **文本**：欲指定至手机剪贴板中的字符串文本，可接变量。

    >**说明：**
    >
    >Android手机设置剪贴板内容大小不可以超过20K。

## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**设置剪贴板文本**组件。
3. 为该组件配置属性，如下图所示。

    - 文本：填写欲指定至手机剪贴板中的字符串文本，如，`S`。

    ![设置剪贴板文本](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setclipboardtext20210319.png)

4. 在该组件下方，拖入一个**写入日志**组件。
5. 为**写入日志**组件设置属性。

    - 日志内容：填写期望输出的日志内容，如，`S`。

6. 保存并运行流程。
7. 在输出窗口中查看流程运行结果。

   ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setclipboardtextresult20210319.png)