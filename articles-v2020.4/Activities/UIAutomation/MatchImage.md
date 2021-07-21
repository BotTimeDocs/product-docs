# 匹配图片

## 视频示例

## 概述

在指定范围内寻找指定图片，返回符合的结果集。不支持图像识别

注意

- 范围限制在静止页面，对于有滚动条的长页面并不会滚动查找

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：接收变量作为目标元素。属性**控件元素**和**选择器**二者互斥。指定查找图片的范围
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定UI元素，指定查找图片的范围。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输入

- **图片** ：属性**图片**和**图片路径**二者互斥且必填一。此项指要匹配的图片，仅支持Image类型变量
- **图片路径** ：属性**图片**和**图片路径**二者互斥且必填一。此项指要匹配的图片，仅支持字符串变量和字符串
- **准确率** ：匹配图片时的准确率

### 输出

- **结果集** ：将符合匹配图片的结果集存储在此变量。可使用此子集作为其他组件的控件元素输入

## 使用示例

1. 拖入**截屏**组件，输出变量设置为Image对象`imgEle`：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage1.png)

2. 拖入**匹配图片**组件，输入的图片为上一步返回的图片对象imgEle, 输出为可遍历的元素结果集`images`
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage2.png)

3. 拖入**点击**组件，输入的元素为上一步返回的结果集中的第一个元素`images.ToList()[0]`：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage3.png)

4. 运行流程，成功点击了匹配到的第一个元素：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage4.png)