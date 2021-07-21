# 设置日志级别

## 视频示例

## 概述

控制日志输出的内容。此组件后的日志将按照所选级别输出。编辑器默认日志输出级别为Info，设置此组件&quot;日志级别&quot;属性为Debug后，可以查看更加详细的日志信息

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 日志

- **日志级别** ：共有三个选项：Debug,  Info, Error。选择Debug后，可查看最详细的日志信息；选择Info后，可查看Info和Error等级的日志信息；选择Error后，将只输出Error日志

## 使用示例

1. 拖入**设置日志级别**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-1.png)


2. 拖入3个**写入日志**组件到设计面板，日志级别分别选择“Debug”，“Info”，“Error”，并分别命名为“Debug日志”，“Info日志”，“Error日志”，下图展示的是设置的Debug日志：
- 设置Debug日志输出的日志信息为："我是一个Debug的日志"；
- 设置Info日志输出的日志信息为："我是一个Info的日志"；
- 设置日志输出的日志信息为："我是一个Error的日志"；

![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-2.png)


3. 选择**设置日志级别**组件的日志级别为“Debug”，运行流程，控制台输出Debug，Info，Error等级的日志信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-3.png)


4. 选择**设置日志级别**组件的日志级别为“Info”，运行流程，控制台输出Info, Error等级的日志信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-4.png)

5. 选择**设置日志级别**组件的日志级别为“Error”，运行流程，控制台只输出Error等级的日志信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-5.png)
