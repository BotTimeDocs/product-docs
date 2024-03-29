# 执行JavaScript文件

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ExecuteJavaScriptFile.mp4"></video>

## 概述

执行JavaScript文件，并支持参数传递。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的UI元素，并在此元素上执行JavaScript。可通过点击指定元素自动生成。仅支持字符串变量和字符串

### 输入

- **方法名称** ：要执行的JavaScript文件中的方法名。支持传递参数。仅支持字符串变量和字符串，如，`"a('b','"+c+"')"`，其中，a为方法名，b为常量，c为变量。

  >**说明：**
  >
  >传入参数如果是String类型常量进行传值，需要自行在变量外拼接`'`或`"`,否则JS运行时会默认为变量进行处理。

- **文件路径** ：将执行此路径下的JavaScript文件。支持相对和绝对路径。可在组件面板点击弹出对话框，选择目标文件；亦支持手动输入路径，若路径不存在，则运行失败。仅支持字符串变量和字符串。

### 输出

- **返回值** ：将执行JavaScript文件后返回的值存储在此变量

## 使用示例

**此流程执行逻辑**：执行`demo.js`文件中的`SetText(st)`方法。

![配置执行JavaScript文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executejavascriptfile20210630.png)

>**说明：**
>
> 图中的`" _context$.currentElement." `表示指定的元素。
