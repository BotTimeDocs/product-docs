# 选择文件

## 视频示例

## 概述

指定筛选的文件类型，在运行时弹窗选择文件后输出

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **描述** ：指定选择文件弹窗的标题
- **文件筛选** ：指定欲过滤的文件类型；默认为所有文件，不过滤。可从下拉列表选择，也可手动输入

### 输出

- **选择的文件** ：输出选择的文件绝对路径；仅支持字符串变量和字符串

## 使用示例

1. 拖入**选择文件**组件，添加输出结果变量filePath：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFile-1.png)

2. 拖入**写入日志**组件，可以输出选择的文件路径信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFile-2.png)

3. 运行流程，**选择文件**组件开始运行，弹出选择文件的框：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFile-3.png)

4. 手动选择一个文件，查看输出的文件路径信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFile-4.png)
