# 代码文件

## 概述

**代码文件** 是指存储不同语言的代码文件。可以在“文件 > 新建 > 代码文件”或项目面板右键菜单中的“添加 > 代码文件”中添加 C#代码文件、Python 代码文件、PowerShell 代码文件。该代码文件用于在组件中执行此代码文件。

## 操作样例

创建一个 C#代码文件并运行。

1. 选择菜单栏中的“文件 > 新建 > 代码文件”菜单。
2. 在弹出的“添加代码文件”弹框中，选择“C#文件”文件类型，自定义一个代码文件名称，如，`test_demo`, 单击“确定”按钮。

    ![添加 C#代码文件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/createcsharpcodefile20210611.png)

3. 在弹出的“C#代码编辑器”框中，编写 C#代码，单击“确认”按钮。

   ![C#代码](https://docimages.blob.core.chinacloudapi.cn/images/Studio/csharpcode20210611.png)

4. 可以看到添加完成的 C#代码文件在项目面板中显示。

    ![已添加完成的 C#代码文件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/csharpcodefiledone20210611.png)

5. 在流程文件中，拖入一个“执行 C#代码”组件至流程中，并选择上方也创建的 C#代码文件。

    ![拖入执行 C#代码组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/selectcsharpcode20210611.png)

6. 保存并运行流程。
7. 在“输出窗口”中，查看流程运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/executecsharpcoderesult20210611.png)
