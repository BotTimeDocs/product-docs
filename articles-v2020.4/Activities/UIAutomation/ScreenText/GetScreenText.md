# 获取屏幕文本

## 视频示例

## 概述

获取指定的文本或指定的文本元素列表。

注意：建议在无法使用 [获取文本](../GetText.md) 组件获取文本时，使用本组件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：接收变量作为获取文本的目标元素。属性**控件元素**和**选择器**二者必填其一且互斥
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示要获取文本的目标元素。可通过点击**指定元素**自动生成。属性**控件元素**和**选择器**二者必填其一且互斥。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输出

- **纯文本** ：将获取到的文本内容存储到此变量。仅支持字符串变量和字符串
- **文本元素列表** ：将获取到的文本元素列表存储到此变量。你可以使用列表的子集作为点击等组件的输入。在对这些元素进行操作时，只支持模拟鼠标键盘的方式，不支持设置控件。

## 使用示例

1. 拖入**获取屏幕文本**组件并指定Adobe Acrobat右侧工具栏：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getScreenTxt1.png)

2. 验证元素有效性：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getScreenTxt2.png)

3. 运行流程并查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getScreenTxt3.png)
