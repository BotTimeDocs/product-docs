# 提取文本

## 视频示例

## 概述

支持提取指定文本内容中符合条件（正则表达式）的第一个结果，源文本内容不变

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **提取规则** ：点击“设置提取规则”后在弹窗中指定提取的规则
- **源文本** ：欲被提取的源文本数据。仅支持字符串变量和字符串

### 输出

- **提取结果** ：执行文本提取规则后提取的数据结果。仅支持字符串变量

## 使用示例

1. 拖入**提取文本**组件至项目流程中

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010401.png)

2. 创建变量，并输入至源文本及验证结果中。选中**提取文本**组件，点击展开提取规则。以手机号码地址为例：点击电话号码，点击手机号码，点击确定。如下图所示

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010402.png)

3. 拖入其它组件至流程中，例：**写入日志**组件，输入日志内容为运行结果（result）

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010403.png)

4. 点击运行，查看运行结果。成功将源文本中手机号提取出来，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010404.png)

