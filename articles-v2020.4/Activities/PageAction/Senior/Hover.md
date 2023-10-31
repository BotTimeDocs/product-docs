# 悬停

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Hover.mp4"></video>

## 概述

模拟鼠标悬停在桌面端或浏览器端的指定元素上。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 目标

- **控件元素** ：接收变量作为鼠标悬停的目标元素。此项和“选择器”二选一填入。
- **选择器** ：用于指示鼠标悬停的目标位置。可通过点击“指定元素”自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待,1000ms = 1s。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：指定网页上需要悬停才可以展示的元素。

![配置悬停组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/hover-2.png)
