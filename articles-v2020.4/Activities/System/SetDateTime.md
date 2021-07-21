# 设置日期和时间

## 视频示例

## 概述

指定日期和时间并输出DateTime类型结果

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **日期和时间** ：将指定的日期和时间输出；需手动输入时间；勾选"选择当前日期和时间"则在流程执行时输出当前系统的日期和时间。可接变量。

## 使用示例

1. 拖入**设置日期和时间**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setDate-1.png)

2. 双击进入组件内部，配置属性参数。
<br/> 日期和时间：将指定的日期和时间输出，如，定义变量“datetime”，勾选上“选择当前时间”，输出当前日期：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setDate-2.png)


3. 拖入**写入日志**组件，可以输出用户设置的日期和时间：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setDate-3.png)

4. 运行流程，输出用户指定的日期和时间：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setDate-4.png)
