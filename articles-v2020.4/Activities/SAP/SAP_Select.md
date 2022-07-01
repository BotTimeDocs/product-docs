# 选择 SAP 项

## 视频示例

## 概述

在指定元素后，通过点击下拉框选择要点击的项目，返回详细的菜单条目到下拉框。

> **说明：**
>
> 本功能仅在云扩企业版编辑器中支持。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **项** ：要点击的项目。此项和下拉框中所选择的项目一致。

### 目标

- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：用于指示特定的 UI 元素。可通过点击 **指定元素** 自动生成。
- **匹配超时(毫秒)** ：限定查找目标选择器的时间，超出指定时间后将不再等待，1000ms = 1s。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：指定 SAP 应用中的“SAP 菜单”元素，然后从返回的详细菜单条目下拉框中选择所需要打开的页面选项。

![配置选择 SAP 项组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sapSelectItem-2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sapSelectItem-3.png)
