# 日期和时间选择框

## 视频示例

## 概述

流程运行时弹窗让用户选择日期和时间并输出。
>**说明：**
>
>运行时窗口中默认显示为当前日期和时间。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **标题**：（非必填）自定义**日期和时间选择框**组件运行时的标题，可接变量。
- **描述**：（非必填）自定义**日期和时间选择框**组件运行时的描述信息，可接变量。

### 输出

- **选择的时间** ：输出用户在弹窗中指定的日期和时间，仅可接变量。

## 使用示例

1. 拖入**日期和时间选择框**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/timePicker-1.png)

2. 双击进入组件内部，配置属性参数。

   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/timePicker-2.png)

- 标题：自定义日期和时间选择框组件运行时的标题，如，“时间”；
- 描述：自定义日期和时间选择框组件运行时的描述信息，如，“当前时间为：”；
- 输出：输出用户在弹窗中指定的日期和时间，如，这里我们指定当前时间：

3. 拖入**写入日志**组件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/timePicker-3.png)

4. 运行流程，弹窗让用户选择日期和时间并输出：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/timePicker-4.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/timePicker-5.png)
