# 获取状态栏信息

## 视频示例

## 概述

在指定SAP状态栏后，返回读取到的状态栏信息。

本功能仅在云扩企业版编辑器中支持。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示SAP状态栏。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标选择器的时间，超出指定时间后将不再等待。若超过此时间还未匹配到则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输出

- **ID** ：将返回的消息号ID存储在此变量。仅支持字符串变量和字符串
- **Number** ：将返回的消息号数字存储在此变量。仅支持字符串变量和字符串
- **文本** ：将返回的文本信息存储在此变量。仅支持字符串变量和字符串
- **类型** ：将返回的信息类型存储在此变量。一共含有以下三种： **S** - 代表成功；**W** - 代表警告；**E** - 代表错误。仅支持字符串变量和字符串

## 使用示例

1. 登录SAP应用，点击SAP菜单->会计核算->财务会计->总账->单据录入->FB50 - 输入总账科目凭证进入“输入总账科目凭证”：公司代码 xxxx”页面。
1. 拖入**点击**组件，指定“明细”，并打开选择器通过验证：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SAPGetStatus-1.png)

2. 拖入**获取状态栏信息**组件，指定状态栏元素，并设置输出变量：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SAPGetStatus-2.png)

3. 拖入**写入日志**组件，以一定的方式输入第2步操作中获取的变量：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SAPGetStatus-3.png)

4. 点击运行流程，查看变量值：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SAPGetStatus-4.png)