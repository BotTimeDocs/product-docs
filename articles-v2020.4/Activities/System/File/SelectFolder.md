# 选择文件夹

## 视频示例

## 概述

选择文件夹路径，在运行时弹窗选择文件夹后输出

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **描述** ：设置选择文件夹弹窗的说明信息

### 输出

- **选择的文件夹** ：输出选择的文件夹路径；仅支持字符串变量和字符串

## 使用示例

1. 拖入**选择文件夹**组件，添加输出结果变量folderPath：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFolder.png)

2. 拖入**写入日志**组件，可以输出选择的文件夹路径信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFolder-2.png)

3. 运行流程，**选择文件夹**组件开始，弹出选择文件的框：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFolder-3.png)

4. 手动选择一个文件，查看输出的文件路径信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFolder-4.png)



