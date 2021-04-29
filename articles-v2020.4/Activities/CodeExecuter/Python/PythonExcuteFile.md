# 执行 Python 代码

在 **Python 环境** 组件内，拖入 **执行 Python 代码**组件，用于执行自定义的 Python 代码。

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件。
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件。

## 操作样例

1. 拖入**Python环境** 组件至流程中。
2. 在 **Python 环境** 组件内，拖入**执行Python代码** 组件。
3. 双击该组件空白处，可出现已默认填充的代码文件路径。

   ![PythonUI](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonexcute20201211.png)

4. 配置**执行Python代码**组件的属性参数。

    - 文件路径：单击“…”按钮，选择 Python 文件的路径并打开，如，D:\workspace\Encoo\组件流程\.code\Python
    -  编辑代码：单击“编辑代码”按钮，在 Python 代码编辑器中输入需要执行的 Python 代码段，如下图所示。

    ![Python代码编辑器](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythoncodeedit20210429.png)

    - **（可选）** 设置参数：单击“设置参数”按钮，在设置参数对话框中创建参数，用于 Python 代码中传递参数。

    ![Python设置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonargument20210429.png)   

    >**说明：**
    >
    > - 根据代码情况，需要传参时，才需要设置参数。
    > - 由于编辑器的底层为 C# 语言编写与 Python 语言之间需要进行转换，所以在 Python 中设置参数时，需要将编辑器中创建的参数赋值给 Python 中创建的参数的值（如上图所示）。

5. 保存并运行流程。
6. 在弹出的参数对话框中，输入参数值。

    ![设置参数](https://docimages.blob.core.chinacloudapi.cn/images/Activities/runandset20210429.png)

7. 在输出窗口中查看最终的输出值。

    ![输出结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/outputpython20210429.png)     