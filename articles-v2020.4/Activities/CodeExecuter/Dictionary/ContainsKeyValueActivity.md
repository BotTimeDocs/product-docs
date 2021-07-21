# 是否包含键/值

## 视频示例

## 概述

判断在变量面板中定义的字典对象中是否包含键（key）及对应的值（value）。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **检测内容**：与“键/值”属性对应的需要检测的参数内容。
- **键/值** ：需要判断字典中是否包含参数 key 和参数 Value 的值。
- **字典**：在变量面板中定义的字典对象，仅可接变量。

### 输出

- **结果**：是否包含“键/值”的结果，仅可接变量。

## 使用示例

1. 拖入一个 **初始化字典** 组件至流程中，具体属性配置参见 [初始化字典](CodeExecuter/../InitializeDictionaryActivity.md)。
2. 拖入一个 **是否包含键/值** 组件至流程中。
3. 双击 **是否包含键/值** 组件的空白处，配置属性。

    ![配置属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/containtskeyvalue20210111.png)

4. 在 **是否包含键/值** 组件的下方，拖入一个 **写入日志** 组件。
5. 双击 **写入日志** 组件的空白处，配置属性。

    - **日志级别**：下拉选择日志级别，如，`Info`。
    - **日志内容**：输入日志内容，如，`R.ToString()`，表示将 **是否包含键/值** 组件的返回值转成字符串输出。

6. 保存并运行流程。
7. 在输出面板中查看运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/containtskeyvalueresult20210111.png)