# 等待元素出现

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/WaitElementAppear.mp4"></video>

## 概述

等待指定的UI元素从屏幕上出现，支持桌面端和浏览器。同时支持桌面端图像识别指定元素，浏览器端暂不支持

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

>**注意：**
>
>**”超时“** 属性设置需要根据需要去设置，否则默认是项目的超时时间（30秒）。举个例子加入我们匹配超时设置成5000（毫秒），超时设置成 20000（毫秒），执行的时候，我们会每5000（毫秒）循环等待目标元素，直到达到“超时”时间（20000毫秒）才会继续往下执行。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的UI元素，该组件将等待此选择器指定的元素出现。可通过点击**指定元素**自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误，1000ms = 1s。

### 输出

- **结果** ：将此组件执行的成功与否的结果存储在此变量。当指定目标出现时，存储的值为True。

- **控件元素** ：将等待出现的元素存储到此变量。可作为**等待元素消失**等组件的输入值。当使用图片识别的方式来指定元素时，返回的是锚点元素而非图片元素。

## 使用示例

**此流程执行逻辑**：等待指定的元素出现时，执行相应的流程。

![配置等待元素出现组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/waitElementAppear2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/waitElementAppear3.png)
