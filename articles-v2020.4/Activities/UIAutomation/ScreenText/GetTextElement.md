# 获取屏幕含某文本的元素

## 视频示例

## 概述

获取指定范围内包含指定文本的 UI 元素，并将其存储在输出变量**文本元素**中。

注意：
- 查找文本时，支持正则表达式。
- 组件只支持桌面端。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：查找文本元素的范围。
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定UI元素。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输入

- **文本**：需要查找的文本。
- **出现次数**：在查找范围内，找到的第 *出现次数* 个元素会被捕获。

### 输出

**文本元素** ：将取到的文本元素存储在此变量，可用于其他组件的输入。

## 使用示例

1. 拖入**获取屏幕含某文本的元素**组件并指定Adobe Acrobat右侧工具栏：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetTextElement1.png)

2. 验证元素有效性：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetTextElement2.png)

3. 运行流程并查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetTextElement3.png)
