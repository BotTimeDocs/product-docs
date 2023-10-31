# 获取区域结构

## 视频示例

## 概述

返回指定桌面端元素的层级结构。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 目标

- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的 UI 元素。可通过点击 **指定数据源** 自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待，1000ms = 1s。

### 输出

- **文本** ：将指定元素的层级结构存储在此变量。JSon 格式。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：获取指定记事本文件中的有内容的区域，返回 JSon 格式文本。

![配置获取区域结构组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetJsonStructure2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetJsonStructure3.png)