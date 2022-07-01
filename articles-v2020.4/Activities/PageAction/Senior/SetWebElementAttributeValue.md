# 设置 Web 元素属性值

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SetWebAttributeValue.mp4"></video>

## 概述

为指定元素设置属性值。例如，使用此组件完成输入框的输入文本操作。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **属性名** ：需要设置的目标元素的属性名。
- **属性值** ：需要设置的目标元素的属性对应的属性值。

### 目标

- **控件元素** ：接收变量作为目标元素。属性 **控件元素** 和 **选择器** 二者互斥。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待，1000ms = 1s。
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定 UI 元素。可通过点击 **指定元素** 自动生成。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。
  
## 使用示例

**此流程执行逻辑**：将网页端的“百度经验”按钮，通过更改按钮元素属性值的方法，更改为“百度搜索”。

![配置设置属性组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setwebelement20210225.png)

**执行结果**：

![查看运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setwebelementresult20210225.png)
