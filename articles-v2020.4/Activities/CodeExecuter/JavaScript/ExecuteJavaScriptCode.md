# 执行JavaScript代码

## 视频示例

## 概述

执行JavaScript代码，可接收执行后的返回值。支持在代码中直接使用本地变量

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的UI元素，并在此元素上执行JavaScript代码。可通过点击指定元素自动生成。仅支持字符串变量和字符串

### 输入

- **代码** ：将执行此代码。可直接使用编辑器本地变量。仅支持字符串变量和字符串。
- **方法名称** ：要执行的JavaScript代码段中的方法名，支持传递参数。仅支持字符串变量和字符串常量，如，`"a('b','"+c+"')"`，其中，a为方法名，b为常量，c为变量。
  
  >**说明：**
  >
  >传入参数如果是String类型常量进行传值，需要自行在变量外拼接`'`或`"`,否则JS运行时会默认为变量进行处理。

### 输出

- **返回值** ：将执行JavaScript代码后返回的值存储在此变量。

## 使用示例

1. 拖入**执行JavaScript代码**组件并指定元素：

    ![执行JavaScript代码](https://docimages.blob.core.chinacloudapi.cn/images/Activities/excutejavascriptcode20210630.png)

2. 打开选择器，点击“未验证”按钮验证元素是否能识别：

    ![验证网页元素](https://docimages.blob.core.chinacloudapi.cn/images/Activities/verifyelement20210630.png)

3. 运行流程并查看结果：

    ![运行流程](https://docimages.blob.core.chinacloudapi.cn/images/Activities/javascriptcoderesult20210630.png)
