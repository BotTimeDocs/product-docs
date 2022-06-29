# 等待元素消失

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/WaitElementDisapper.mp4"></video>

## 概述

等待指定的桌面端或浏览器端的 UI 元素从屏幕上消失。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

> **注意：**
>
> **”超时“** 属性的设置需要根据情况去设置，否则默认是项目的超时时间（30 秒）。例：假如我们匹配超时设置成 5000（毫秒），超时设置成 20000（毫秒），执行的时候，我们会在5000（毫秒）查找目标元素，此时，
>
> - 如果目标元素还未出现，并在剩下的15000（毫秒）中继续查找目标元素，直到找到目标元素且在“超时”时间内消失时，才执行下游流程。
> - 如果目标元素在整个“超时”时间内一直未找到，则默认目标元素已经消失了，在达到“超时”时间后，继续执行下游流程。

![等待元素消失超时属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/waitelementdisappear20211028.png)

### 输出

- **结果** ：将此组件执行的成功与否的结果存储在此变量。当指定目标消失时，存储的值为 True。

### 目标

- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的 UI 元素，该组件将等待此选择器指定的元素消失。可通过点击 **指定元素** 自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待，1000ms = 1s。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：实现等待指定的桌面端的“发送”按钮元素从屏幕消失。

![配置等待元素消失组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/waitElementVanish2.png)
