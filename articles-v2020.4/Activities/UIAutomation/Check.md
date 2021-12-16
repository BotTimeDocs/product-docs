# 勾选

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Check.mp4"></video>

## 概述

选择或清除桌面端或浏览器端的单选按钮和复选框。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **勾选**：选择单选框或复选框的状态。

### 目标

- **控件元素** ：接收变量作为勾选的目标元素。属性**控件元素**和**选择器**二者必填其一且互斥。
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：用于指示要勾选的目标元素。可通过点击**指定元素**自动生成。
- **匹配超时（毫秒）** ：限定查找目标元素时间，超出指定时间后将不再等待，1000ms = 1s。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：指定需勾选的网页元素，并为其执行勾选操作。

![配置勾选组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/check-2.png)
