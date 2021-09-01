# 执行 Python 代码

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ExecutePythonCode.mp4"></video>

## 概述

在 **Python 环境** 组件内，拖入 **执行 Python 代码** 组件，用于执行自定义的 Python 代码。

> **小技巧：**
>
> 将项目面板中的 Python 代码文件（扩展名为.py）拖拽至编辑区域，将自动生成“执行 Python 代码”组件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

## 使用示例

**前置必要组件**：[Python 环境](../Python/PythonScope.md)
**此流程执行逻辑**：执行本地 Python 文件中的 Python 代码段。

![Python 代码编辑器](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythoncodeedit20210429.png)

**（可选）** 设置参数：单击“设置参数”按钮，在设置参数对话框中创建参数，用于 Python 代码中传递参数。

![Python 设置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonargument20210429.png)   

> **说明：**
>
> - 根据代码情况，需要传参时，才需要设置参数。
> - 由于编辑器的底层为 C# 语言编写与 Python 语言之间需要进行转换，所以在 Python 中设置参数时，需要将编辑器中创建的参数赋值给 Python 中创建的参数的值（如上图所示）。
> - 支持设置多个输出方向的参数。
> - Ctrl+Space 可以实现联想功能。

## 常见问题

**1. Pycharm可以运行的脚本，而在Python组件里却不能运行**

**A：** 使用本地的python编译环境，不使用Pycharm里虚拟的编译环境。

![python1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonscript20210819.png)

**2. Python环境失败， xxx不是有效的环境路径**

**A：** 正确的环境路径是python的安装路径，找到正确的安装路径（目录下有python.exe，和Lib文件夹）。

![python2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonenvironment20210819.png)

**3. 缩进中Tab/空格使用不一致**

**A：**  删除出错行，统一使用Tab作为缩进。

![python3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonerror20210819.png)
