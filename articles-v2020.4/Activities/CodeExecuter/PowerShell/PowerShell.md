# 执行 PowerShell 代码

## 视频示例

## 概述

该组件实现自定义的 PowerShell 代码。

> **小技巧：**
>
> 将项目面板中的 PowerShell 代码文件（扩展名为.ps1）拖拽至编辑区域，将自动生成“执行 PowerShell 代码”组件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件路径**：需要执行的 PowerShell 文件路径，支持相对路径或绝对路径。
- **参数**：设置需要传参的参数信息。

### 输出

- **结果**：执行结果，仅可接变量。

## 使用示例

**前置必要条件**：首次使用该组件执行 PowerShell 代码时，需配置执行策略，可参见 [关于执行策略](https://docs.microsoft.com/zh-cn/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.1)。

**此流程执行逻辑**：执行指定的 PowerShell 代码。

![配置执行 powershell 代码](https://docimages.blob.core.chinacloudapi.cn/images/Activities/powershell20210225.png)

![设置参数信息](https://docimages.blob.core.chinacloudapi.cn/images/Activities/powershellparmar20210225.png)
