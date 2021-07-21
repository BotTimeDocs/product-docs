# 获取焦点控件

## 视频示例

## 概述

获取指定窗体内的焦点控件。

支持桌面端，浏览器暂不支持。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：接收变量作为指定窗体。属性**控件元素**和**选择器**二者互斥，且均可为空，均为空时默认查找当前活动窗体的焦点控件
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的UI元素。可通过点击**指定窗体**自动生成。属性**控件元素**和**选择器**二者互斥，且均可为空，均为空时默认查找当前活动窗体的焦点控件。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输出

- **焦点控件** ：将指定窗体的焦点控件存储在此变量

## 使用示例

1. 拖入[切换控件](activity/../SwitchControl.md)组件，指定企业微信窗口，打开一个新的聊天窗口：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetFocus1.png)

2. 展示企业微信聊天窗口，可以看到焦点定位于搜索框内：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetFocus2.png)

3. 拖入**获取焦点控件**，指定输出为焦点元素变量：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetFocus3.png)

4. 拖入输入文本组件，指定输入为焦点元素变量：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetFocus4.png)

5. 运行流程并查看结果，对获取焦点输出的元素操作成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetFocus5.png)
