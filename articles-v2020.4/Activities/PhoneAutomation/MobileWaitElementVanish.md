# 等待元素消失

## 视频示例

## 概述

等待指定元素的消失，支持图像识别和指定元素。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **[选择器](../Appendix/Selector.md)**：要获取的特定UI元素。可通过点击指定元素自动生成，仅支持字符串变量和字符串。
- **匹配超时(毫秒)**：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms =1s，仅支持整型变量和整型。

### 输出

- **结果**：将此组件执行的成功与否的结果存储在此变量。当指定目标出现时，存储的值为True，仅支持布尔型变量和布尔。
  
## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**等待元素消失**组件。
3. 单击**等待元素消失**组件中的**指定元素**链接，选择需要指定等待消失的元素，这里以等待某一图片轮播消失为例，如下图所示。

    ![选择软件名称](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stepshow20201224.png)

4. 配置**等待元素消失**组件的属性参数。

    ![配置等待元素出现](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingwaitelementvanish20201224.png)

5. 在**等待元素消失**组件的下方，拖入一个**写入日志**组件，并配置属性参数，将**等待元素消失**组件返回的结果输出至日志中。

    - 日志级别：下拉选择日志级别，如，Info
    - 日志内容：输入日志内容，如，W.ToString()

6. 保存并运行流程，可看到将**等待元素消失**组件返回的结果输出至日志中的运行效果，如下图所示。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/showwaitelementvanish20201224.png)
