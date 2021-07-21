# 筛选

## 视频示例

## 概述

设置&quot; 筛选向导&quot; 中的条件，并依此对工作表进行条件筛选，同时将符合筛选条件的结果应用到工作表内。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：执行筛选的目标工作表。仅支持字符串变量和字符串
- **列号** ：执行筛选的目标列。仅支持整型变量和整型

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Filter1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **筛选** 到 **打开/新建** 组件中，填写 sheet 名称，填写列号，填写筛选条件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Filter2.png)

1. 点击运行，运行后打开 Excel 查看筛选结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Filter3.png)