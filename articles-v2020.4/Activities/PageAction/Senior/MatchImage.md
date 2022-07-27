# 匹配图片

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/MatchPicture.mp4"></video>

## 概述

在指定范围内寻找指定图片，返回符合的结果集。

>**说明：**
>
>范围限制在静止页面，对于有滚动条的长页面并不会滚动查找.

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 目标

- **控件元素** ：接收变量作为目标元素。属性**控件元素**和**选择器**二者互斥。指定查找图片的范围
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定UI元素，指定查找图片的范围。可通过点击**指定元素**自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待,1000ms = 1s。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 输入

- **图片** ：属性**图片**和**图片路径**二者互斥且必填一。此项指要匹配的图片，仅支持Image类型变量
- **图片路径** ：属性**图片**和**图片路径**二者互斥且必填一。此项指要匹配的图片。
- **准确率** ：匹配图片时的准确率。

### 输出

- **结果集** ：将符合匹配图片的结果集存储在此变量。可使用此子集作为其他组件的控件元素输入。

## 使用示例

**前置必要组件**：[截屏](../../PageAction/Screenshot.md)

**此流程执行逻辑**：匹配已截屏的图片。

![配置匹配图片组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage2.png)