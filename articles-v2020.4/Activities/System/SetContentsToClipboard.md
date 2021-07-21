# 设置剪贴板文本

## 视频示例

## 概述

设置文本内容到剪贴板。

> 使用时，建议为此组件添加1秒以上的前延迟。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **文本** ：将要填写到剪贴板的文本内容，可接变量

## 使用示例

1. 拖入**设置剪贴板文本**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setClipboard-1.png)

2. 双击进入组件内部，文本框填入变量“result”，文本框支持字符串或者变量：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setClipboard-2.png)

3. 拖入**写入日志**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setClipboard-3.png)

4. 运行流程，控制台输出用户设置的剪贴板文本：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setClipboard-4.png)