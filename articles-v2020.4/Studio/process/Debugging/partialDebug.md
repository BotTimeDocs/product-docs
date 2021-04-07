# 分步调试

## 调试单个文件

当自动化项目比较复杂，而每一次调试或运行都耗费巨大的时间和人力，此时便可以使用 **调试/运行文件**，来将一个大型的项目拆分，分别进行调试或运行。这样，便可以更快的对项目的正确性进行判断，更快完成项目的校验。

你可以使用项目面板的右键菜单或快捷键（F6/Ctrl+F6）来进行调试或运行文件。
![分布调试入口](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Debugging/partialdebug20210222.png)

当当前所选中的流程文件包含参数，点击“调试/运行文件”，将会弹出一个设置流程参数的窗口，你可以选择设置不一样的参数值来进行校验，也可以使用默认值进行校验。

![打开文件/文件夹](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Debugging/openfile&folder20201214.png)

> **注意：**
>
> - 设置流程参数窗口仅支持更改输入方向的参数的值。
> - 当参数类型为 `Encoo.DataType.FilePath` 或 `Encoo.DataType.FolderPath` 时，可单击如上图所示的图标，打开并输入文件或文件夹的路径。

## 调试单个组件

在自动化项目实施过程中，经常会遇到已定位到某个组件有报错异常，但无法更准确地定位到该组件的具体某一步骤错误，此时可在流程中选择该组件，在右键菜单中选择“组件调试”，进行调试选中的单个组件。

>**说明：**
>
>当使用上下文菜单中的“组件调试”功能时，支持设置变量或参数的值。

![调试单个组件入口](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Debugging/debugactivity20210317.png)

当当前所选组件包含变量或参数时，将弹框显示该组件的作用域的变量和参数，（可选）设置弹框中的变量或参数后，单击“确定”按钮后，将开始调试该组件。

![调试单个组件设置框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Debugging/debugactivityarguments20210317.png)

## 从选定组件开始调试

在编辑器里，如果流程中有多个组件，需要指定从某一个组件开始调试，则可以在编辑区域中选中需要开始调试的组件，在右键快捷菜单中选择 **从此组件调试** 选项, 将从选定的该组件开始进行调试流程。

>**说明：**
>
>当使用上下文菜单中的“从此组件调试”功能时，支持设置变量或参数的值。

![从选定组件调试](https://docimages.blob.core.chinacloudapi.cn/images/Studio/debugformactivity20210323.png)