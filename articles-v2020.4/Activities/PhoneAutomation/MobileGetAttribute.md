# 获取元素属性值

## 视频示例

## 概述

输出指定元素的属性值，并将其存储在输出变量属性值中。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **[选择器](../Appendix/Selector.md)**：要获取的特定UI元素。可通过点击指定元素自动生成，仅支持字符串变量和字符串。

### 输入

- **属性名**：要获取目标元素的属性名，仅支持字符串变量和字符串。
  
### 输出

- **属性值**：获取到的属性值内容，仅支持字符串变量和字符串。

## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**获取元素属性值**组件。
3. 单击**获取元素属性值**组件中的“指定元素”链接，指定需要获取的元素。
   ![指定获取元素](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settinggettext20201223.png)

4. 在**获取元素属性值**组件中的下拉框中，选择需要获取的属性名，如下图所示。
   ![获取元素属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getelementattribute20201223.png)
5. 配置**获取元素属性值**组件的属性参数。
   ![配置获取元素属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dimvarial20201223.png)
6. 在**获取元素属性值**组件的下方，拖入一个**写入日志**组件，并配置属性参数，将获取到的元素属性值输出至日志中。
    - 日志级别：下拉选择日志级别，如，Info
    - 日志内容：输入日志内容，如，"获取到的元素属性值为："+GetElementAttribute
7. 保存并运行流程，可看到将获取到的元素属性值输出至日志中的运行效果，如下图所示。
   ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/showgetattribute20201223.png)