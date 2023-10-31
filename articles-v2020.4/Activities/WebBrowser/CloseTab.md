# 关闭标签页

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/CloseTab.mp4"></video>

## 概述

使用该组件关闭网站内特定标签页。该组件必须放置在**绑定浏览器**或**打开浏览器**组件中使用。

有两种使用场景：

1. 不指定标签页，即选择器属性为空时，默认关闭当前活动标签页
2. 指定标签页，即使用“指定标签页”功能时，将关闭指定的特定标签页

## 浏览器版本要求

参见 [浏览器版本要求](../WebBrowser/browser-version.md)。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **匹配超时(毫秒)** ：定位 **选择器** 属性指定的标签页的时间，毫秒为单位。若超过此时间还未匹配到指定标签页则会抛出错误。仅支持整型变量和整型
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：通过提供的选择器表达式来定位目标标签页，亦可通过 **指定标签页** 自动获取，并可以进行编辑实现自定义。当此项为空时，默认关闭当前活动标签页；当通过“指定标签页”自动生成此值后，关闭指定标签页。仅支持字符串变量和字符串

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**前置必要组件**：[绑定浏览器](../WebBrowser/AttachBrowser.md)

**此流程执行逻辑**：关闭浏览器的指定标签页。

![配置关闭标签页组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CloseTab20201221.png)
