# 调用子流程

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/InvokeSubWorkflow.mp4"></video>

## 概述

支持调用执行其他子流程文件，并可在两个流程间进行参数的传递。可在组件面板点击弹出对话框，选择要调用的文件；亦支持手动输入路径。

>**小技巧：**
>
>将项目面板中的流程文件（扩展名为.xaml）拖拽至编辑区域，将自动生成“调用子流程”组件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **流程文件路径** ：设置被调用的文件路径，支持绝对路径和相对路径。
- **参数**（可选） ：点击“设置参数”后在弹窗设置参数，并设置名称、方向、类型及值。在弹窗中点击“导入参数”可直接把被调用文件的参数写入到参数列表。

## 使用示例

**此流程执行逻辑**：在A流程中，调用B流程并执行。

![子流程配置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/invokesubworkflow20210715.png)
