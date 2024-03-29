# 执行 JavaScript 代码

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ExecuteJavaScriptCode.mp4"></video>

## 概述

执行 JavaScript 代码，可接收执行后的返回值。

> **说明：**
>
> 支持在代码中直接使用本地变量。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **代码** ：将执行此代码。可直接使用编辑器本地变量。
- **方法名称** ：要执行的 JavaScript 代码段中的方法名，支持传递参数。如，`"a('b','"+c+"')"`，其中，a 为方法名，b 为常量，c 为变量。
  
  > **说明：**
  >
  > 传入参数如果是 String 类型常量进行传值，需要自行在变量外拼接 `'` 或 `"`, 否则 JS 运行时会默认为变量进行处理。

### 输出

- **返回值** ：将执行 JavaScript 代码后返回的值存储在此变量。

### 目标

- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待,1000ms = 1s。
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的 UI 元素，并在此元素上执行 JavaScript 代码。可通过点击指定元素自动生成。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。
  
## 使用示例

**此流程执行逻辑**：在指定的百度网页文本框中输入一个字符串文本 `123`。

![执行 JavaScript 代码](https://docimages.blob.core.chinacloudapi.cn/images/Activities/excutejavascriptcode20210630.png)

>**说明：**
>
> 图中的`" _context$.currentElement." `表示指定的元素。
