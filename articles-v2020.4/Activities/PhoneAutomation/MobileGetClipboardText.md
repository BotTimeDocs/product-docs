# 获取剪贴板文本

## 视频示例

## 概述

获取手机端当前剪贴板中字符串文本。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **文本**：将获取到的剪贴板中的字符串文本存到此变量中。

## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**设置剪贴板文本**组件。
3. 为该组件配置属性，如下图所示。

    - 文本：填写欲指定至手机剪贴板中的字符串文本，如，`"Test"`。

4. 在**设置剪贴板文本**组件下方，拖入一个**获取剪贴板文本**组件。
5. 设置**获取剪贴板文本**组件的属性。

    ![获取剪贴板文本属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getclipboardtext20210319.png)

6. 在该组件下方，拖入一个**写入日志**组件。
7. 为**写入日志**组件设置属性。

    - 日志内容：填写期望输出的日志内容，如，`O`。

8. 保存并运行流程。
9. 在输出窗口中查看流程运行结果。

    ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getclipboardtextresult20210319.png)