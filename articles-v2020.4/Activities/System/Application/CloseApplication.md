# 关闭程序

## 视频示例

## 概述

关闭指定UI元素相对于的应用程序（包括桌面程序和浏览器）

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

###　目标

- **选取器** ：用于指示要关闭的目标程序。可通过点击&quot;指定程序&quot;自动生成。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：默认为5000毫秒，可配置超时时间
- **控件元素** ：传入&quot;打开程序&quot;的输出变量，作为目标程序执行关闭操作。此项和上述字段二选一填入。

## 使用示例

### 用选择器指定关闭新的记事本程序

1. 拖入**关闭程序**组件到设计面板，双击进入组件内部：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/closeApp-1.png)

2. 手动打开一个新的记事本文件， 点击**指定程序**，进入选择程序状态：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/closeApp-2.png)

4. 将鼠标滑动到打开的记事本程序上，当被选中的记事本程序周边出现黄色框的时候，说明选择器已经识别到记事本程序，然后点击。

5. 点击之后，会自动化返回到编辑器程序中，可以看到“关闭程序”组件中已经捕捉到记事本程序的截图：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/closeApp-3.png)

6. 运行，打开的记事本被关闭。
