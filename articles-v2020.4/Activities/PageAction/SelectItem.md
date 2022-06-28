# 选择单选下拉框

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SelectItem.mp4"></video>

## 概述

选择下拉框列表中的一项，支持桌面端和浏览器。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **控件元素** ：接收变量作为目标元素。属性**控件元素**和**选择器**二者必填其一且互斥。
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：用于指示要下拉框目标元素。可通过点击**指定元素**自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待，1000ms = 1s。

### 输入

- **项目文本** ：下拉框中要选择的项目。最终该组件将点击此项，并显示在下拉框中。仅支持字符串变量和字符串

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：指定网页或桌面元素并设置需要选择的选项文本后，验证执行。

![配置选择项目组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectItem2.png)

## 常见问题

1. **Q：下拉列表如需选择其它值，应该使用哪个组件？**

    ![下拉列表](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectitem20210824.png)

    **A：** 使用“选择单选下拉框”组件，若该组件不支持，可使用“点击”组件选择。

2. **Q：如何选择下图小三角里的“另存为”选项？使用【点击】组件，定位失败。使用【选择单选下拉框】组件，提示不支持。**

    ![选择项目](https://docimages.blob.core.chinacloudapi.cn/images/Activities/saveas20210824.png)

    **A：** 类似这些无法识别为“选择单选下拉框”的，建议使用两次“点击”组件实现。
