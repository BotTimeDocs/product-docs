# 获取元素属性值

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetElementAttribute.mp4"></video>

## 概述

获取桌面端或浏览器端指定元素的属性值，并将其存储在输出变量 **属性值** 中。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **属性名** ：要获取目标元素的属性名。
  
  > **说明：**
  >
  > 支持在组件中属性名的下拉列表框中输入已存在但未显示的自定义属性。

### 输出

- **属性值** ：将获取到的属性值存储在此变量。

### 目标

- **控件元素** ：接收变量作为目标元素。属性 **控件元素** 和 **选择器** 二者互斥。
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定 UI 元素。可通过点击 **指定元素** 自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待,1000ms = 1s。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：获取指定元素的属性值。

![配置获取元素属性值组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getElementAttr1.png)

## 常见问题

1. **Q：如何获取当前页面的URL？**

    **A：** 使用“获取元素属性值”组件，获取URL属性。
