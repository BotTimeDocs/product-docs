# 遍历文件夹

## 视频示例

## 概述

遍历指定的文件夹并获取文件路径（默认为变量filePath），可在此组件范围内根据实际业务需要拖入其他组件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **文件筛选** ：输入欲筛选的文件类型，默认为空即获取所有文件；支持通配符（* 和 ?）或指定文件名称，例如：*.xls 或 ?.jpg
- **遍历子文件夹** ：默认为False，即不遍历子文件夹。勾选后则遍历指定“文件夹”下的子文件夹

### 输入

- **文件夹** ：输入欲遍历的文件夹路径，支持绝对和相对路径。可接变量。

## 使用示例

1. 拖入**遍历文件夹**组件到设计面板，双击进入组件内部，在组件面板点击“...”弹出对话框，选择目标文件；或者手动输入路径：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/foreachFolder-1.png)

2. 在**遍历文件夹**组件里拖入**写入日志**组件，可以输出遍历的文件夹里文件路径信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/foreachFolder-2.png)

3. 运行流程，查看输出的文件夹里文件路径信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/foreachFolder-3.png)
