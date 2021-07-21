# 获取剪贴板文本

## 视频示例

## 概述

获取剪贴板的文本内容并以String类型输出

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **文本** ：输出String类型的剪贴板文本内容

## 使用示例

1. 拖入**获取剪贴板文本**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-1.png)

2. 双击进入组件内部，输出文本框填入变量“copy_text”，输出文本框输出String类型的剪贴板文本内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-2.png)

3. 拖入**写入日志**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-3.png)

4. 打开网页，复制一段内容到剪贴板上：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-4.png)

5. 运行流程，控制台输出获取的剪贴板上的文本内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-5.png)
