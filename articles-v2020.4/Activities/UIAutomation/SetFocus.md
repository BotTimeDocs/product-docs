# 设置焦点

## 视频示例

## 概述

为指定元素设置焦点，支持桌面端和浏览器端。同时浏览器端可自动滑动页面将元素置为可视

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：接收变量作为目标元素。属性**控件元素**和**选择器**二者互斥
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定UI元素。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

## 使用示例

1. 拖入**设置焦点**组件，设置对应的属性值：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setFocus1.png)

2. 指定元素，并验证元素存在性：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setFocus2.png)

3. 运行流程并查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setFocus3.png)