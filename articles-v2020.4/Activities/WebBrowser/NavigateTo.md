# 当前页跳转

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/JumpToCurrentPage.mp4"></video>

## 概述

使用该组件实现在当前浏览器对象范围内的当前标签页进行跳转。跳转后，无需重新绑定浏览器，即可正常操作新页面内元素（点击等可以在新页面生效）。

>**说明：**
>
>该组件必须放置在**绑定浏览器**或**打开浏览器**组件中使用。

## 浏览器版本要求

参见 [浏览器版本要求](../WebBrowser/browser-version.md)。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **网址** ：将跳转到此网址。

### 可选项

- **等待加载完成** ：勾选时，执行操作之前，等待目标用户界面元素加载完成之后才执行下一个组件操作。

## 使用示例

**此流程执行逻辑**：从云扩科技官网页面跳转至云扩学院标签页。

![配置当前页跳转组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/NavigateTo20201221.png)
