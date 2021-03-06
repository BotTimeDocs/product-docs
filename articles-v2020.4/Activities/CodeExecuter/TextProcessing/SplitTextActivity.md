# 分割文本

根据指定的分割符分割文本。

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件。
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件。

### 输入

- 原文本：原始需要被分割的文本内容，可接变量。
- 分隔符：分隔原文本内容的分隔符号（该分隔符号包含在原文本中），可接变量。

### 输出

- 分割结果：分割的结果，仅可接变量。

## 操作样例

1. 拖入一个**分割文本**组件至流程中。
2. 配置**分割文本**组件的属性。

    ![配置属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/splittext20210104.png)

    - 原文本：输入需要被分隔的文本字符串，如，`"123.56"`
    - 分隔符：输入需要分隔原文本的分隔符号，如，`"."`
    - 分割结果：输入存放分割结果的变量，如，`S`

3. 在**分割文本**组件的下方，拖入一个**写入日志**组件，用于将分割的文本的值进行输出查看。。
4. 双击**写入日志**组件的空白处，配置属性。

    - 日志级别：下拉选择日志级别，如，`Info`
    - 日志内容：输入需要输出的日志内容，如，`"分割后的值为："+S[0]`,表示获取分割后的文本的第一个文本值。

5. 保存并运行流程。
6. 在编辑器的输出面板中查看运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/splittextresult20210104.png)