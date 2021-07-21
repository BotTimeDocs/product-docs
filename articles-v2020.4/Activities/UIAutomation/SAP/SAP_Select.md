# 选择SAP项

## 视频示例

## 概述

在指定元素后，返回详细的菜单条目到下拉框。通过点击下拉框选择要点击的项目。当指定的元素不支持此组件时，会有提示。

本功能仅在云扩企业版编辑器中支持。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的UI元素。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标选择器的时间，超出指定时间后将不再等待。若超过此时间还未匹配到则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输入

- **项** ：要点击的项目。此项和下拉框中所选择的项目一致。仅支持字符串变量和字符串

## 使用示例

1. 拖入**登录应用**组件并输入相应属性值；拖入**点击**组件，指定“取消”按钮元素：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sapSelectItem-1.png)

2. 拖入**等待元素出现**组件，指定“SAP 轻松访问”文本元素；拖入**选择SAP项**组件，指定“SAP 菜单”元素，然后从返回的详细菜单条目下拉框中选择所需要打开的页面选项，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sapSelectItem-2.png)

3. 点击运行流程，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sapSelectItem-3.png)
