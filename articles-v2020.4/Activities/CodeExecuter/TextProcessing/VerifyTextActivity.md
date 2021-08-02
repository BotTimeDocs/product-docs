# 验证文本有效性

## 视频示例

## 概述

使用正则表达式对整段源文本内容验证是否匹配期望值

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **源文本** ：欲被验证的源文本数据。仅支持字符串变量和字符串
- **提取规则** ：点击“设置验证规则”后在弹窗中指定验证的规则

### 输出

- **验证结果** ：验证的结果。仅支持Boolean变量

## 使用示例

1. 拖入**验证文本有效性**组件至项目流程中

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010401.png)

2. 选中组件，点击展开提取规则。以邮箱地址为例，点击邮箱地址点击确定。创建变量，String类型变量及Boolean类型变量，并输入至源文本及验证结果中。如下图所示：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010402.png)

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010403.png)

3. 拖入写入日志组件将验证结果以字符串格式输出。点击运行，查看运行结果，验证文本结果为成功。如下图所示：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010404.png)

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010405.png)
