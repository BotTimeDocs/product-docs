# 筛选

## 视频示例

## 概述

设置&quot; 筛选向导&quot; 中的条件，并依此对工作表进行条件筛选，同时将符合筛选条件的结果应用到工作表内

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：执行筛选的目标工作表。仅支持字符串变量和字符串
- **列号** ：执行筛选的目标列。仅支持整型变量和整型

## 使用示例

1. 新建一个 Excel 文件，在 A1: B8 处填入需要被读取的值:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps29.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **筛选** 组件至 **打开/新建** 组件中:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps30.png)

4. 双击 "筛选向导" 按钮，并配置筛选条件:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps31.png)

5. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps32.png)
