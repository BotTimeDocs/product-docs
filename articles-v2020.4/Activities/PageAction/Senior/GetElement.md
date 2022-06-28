# 获取元素

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetElement.mp4"></video>

## 概述

获取指定的UI元素，并将其存储在输出变量**控件元素**中。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **控件元素** ：将取到的元素存储在此变量，可用于其他组件的输入。此输出所支持的获取属性值请点击[此处](../Appendix/SupportedAttribute.md?_v=v2020.4)查看。

  >**说明：**
  >
  >仅当其他组件（如，点击、输入文本等）的输入方式设置为非**控件元素**时，才支持使用图像识别控件元素作为输入。

### 目标

- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定UI元素。可通过点击**指定元素**自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待，1000ms = 1s。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：通过单击该组件的“指定元素”，获取界面元素存储到输出变量的“控件元素”属性中。

![配置获取元素组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getElement1.png)
