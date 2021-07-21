# 勾选

## 视频示例

## 概述

选择或清除单选按钮和复选框，支持桌面端和浏览器

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：接收变量作为勾选的目标元素。属性**控件元素**和**选择器**二者必填其一且互斥
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：用于指示要勾选的目标元素。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串
- **匹配超时（毫秒）** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输入

- **勾选** ：选择单选框或复选框的状态为Check选中，Uncheck取消选中，Toggle切换

## 使用示例

1. 拖入**勾选**组件并指定元素，从勾选下拉菜单中选择“勾选”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/check-1.png)

2. 打开选择器，点击“未验证”按钮验证元素是否能识别：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/check-2.png)

2. 步骤1中指定元素的网页保持打开状态，运行流程并查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/check-3.png)
