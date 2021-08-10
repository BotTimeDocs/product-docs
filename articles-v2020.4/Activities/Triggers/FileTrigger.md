# 文件触发器

## 视频示例

<video controls height='450px' width='800px' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/FileTrigger.mp4"></video>

## 概述

文件触发器用于监听指定文件夹下文件变化，设置特定触发条件并自动执行流程。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件夹路径** ：输入被监听的文件夹路径；支持绝对和相对路径；可接变量。
- **文件筛选** ：输入被监听的文件类型；支持通配符（* 和 ?）或指定文件名称。例如：`*.xls` 或 `?.jpg`。
- **监听事件** ：选择监听的事件类型：创建、删除、修改。
- **包含子文件夹** ：指定是否监听子文件夹中符合类型的文件。

### 输出

- **文件路径**：输出监听到的文件路径。

### 可选项

- **超时**：输入超时时间，格式：时:分:秒。

## 使用示例

**此流程执行逻辑**：当指定的文件夹路径下有新增的`.png`文件时，输出该文件路径。

![配置文件触发器组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FileTrigger1.png)
