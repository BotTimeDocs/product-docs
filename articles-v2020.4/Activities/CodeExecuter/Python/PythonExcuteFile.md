# 执行 Python 代码

## 视频示例

## 概述

在 **Python 环境** 组件内，拖入 **执行 Python 代码**组件，用于执行自定义的 Python 代码。

> **小技巧：**
>
> 将项目面板中的 Python 代码文件（扩展名为.py）拖拽至编辑区域，将自动生成“执行 Python 代码”组件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

## 使用示例

**前置必要组件**：[Python环境](../Python/PythonScope.md)
**此流程执行逻辑**：执行本地Python文件中的Python代码段。

![Python代码编辑器](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythoncodeedit20210429.png)

**（可选）** 设置参数：单击“设置参数”按钮，在设置参数对话框中创建参数，用于 Python 代码中传递参数。

![Python设置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonargument20210429.png)   

>**说明：**
>
> - 根据代码情况，需要传参时，才需要设置参数。
> - 由于编辑器的底层为 C# 语言编写与 Python 语言之间需要进行转换，所以在 Python 中设置参数时，需要将编辑器中创建的参数赋值给 Python 中创建的参数的值（如上图所示）。
> - 支持设置多个输出方向的参数。
