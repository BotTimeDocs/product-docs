# 文件/文件夹是否存在

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/FolderExist.mp4"></video>

## 概述

判断指定文件或文件夹是否存在，并返回结果。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **路径类型** ：下拉选择判断类型为文件或文件夹
- **路径** ：执行判断的文件或文件夹路径，支持相对和绝对路径。

### 输出

- **路径是否存在** ：将判断结果存储在此变量。

## 使用示例

**此流程执行逻辑**：指定一个固定的文件路径，判断该文件路径是否存在，将返回结果保存至 exists 变量中。

![配置文件/文件夹路径是否存在组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-3.png)
