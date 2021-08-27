# 脚本

## 概述

**脚本** 是指存储不同语言的代码文件。可以在“文件 > 新建 > 脚本”或项目面板右键菜单中的“添加 > 脚本”中添加 Python 脚本文件、PowerShell 脚本文件。该脚本用于在组件中执行此脚本文件。

## 使用示例

创建一个 Python 脚本文件并运行。

1. 选择菜单栏中的“文件 > 新建 > 脚本”菜单。
2. 在弹出的“添加脚本”弹框中，选择“Python 文件”文件类型，自定义一个脚本文件名称，如，`test_demo`, 单击“确定”按钮。

    ![添加 Python 脚本文件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/createpythoncodefile20210827.png)

3. 在“项目面板”上可以看到添加完成的 Python 文件。

    ![已添加完成的 Python 文件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/pythonfiledone20210827.png)

4. 双击“test_demo.py”文件，在弹出的“Python 代码编辑器”框中，编写 Python 代码，单击“确认”按钮。

   ![Python 代码](https://docimages.blob.core.chinacloudapi.cn/images/Studio/pythoncode20210827.png)

5. 在流程文件中，拖入一个“执行 Python 代码”组件至流程中，并选择上方已创建的 Python 代码文件。

    > **说明：**
    >
    > 也可以从项目面板拖动已创建的 Python 文件至流程中的“Python 环境”组件中。

    ![拖入执行 Python 代码组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/selectpythonfile20210827.png)

6. 保存并运行流程。
7. 在“输出窗口”中，查看流程运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/executepythoncode20210827.png)
