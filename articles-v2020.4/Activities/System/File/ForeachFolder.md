# 遍历文件夹

## 视频示例

<video controls height='450px' width='800px' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/TraverseFolders.mp4"></video>

## 概述

遍历指定的文件夹并获取文件路径（默认为变量filePath），可在此组件范围内根据实际业务需要拖入其他组件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件夹** ：输入欲遍历的文件夹路径，支持绝对和相对路径。可接变量。

### 可选项

- **文件筛选** ：输入欲筛选的文件类型，默认为空即获取所有文件；支持通配符（* 和 ?）或指定文件名称，例如：*.xls 或 ?.jpg
- **遍历子文件夹** ：默认为False，即不遍历子文件夹。勾选后则遍历指定“文件夹”下的子文件夹

## 使用示例

**此流程执行逻辑**：查看指定文件夹路径下的文件路径，并输出至“输出面板”中。

![配置遍历文件夹组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/foreachFolder-1.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/foreachFolder-3.png)
