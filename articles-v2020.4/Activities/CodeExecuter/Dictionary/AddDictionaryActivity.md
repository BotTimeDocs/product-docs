# 添加键值对

## 视频示例

## 概述

对已初始化的字典变量添加键值对。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入/输出

- **字典**：在变量面板中定义的字典对象，仅可接变量。
    - **键/值** ：需要向字典中的添加的参数 key 和参数 Value 的值，可接变量。

## 使用示例

1. 拖入一个 **初始化字典** 组件至流程中，具体属性配置参见 [初始化字典](CodeExecuter/../InitializeDictionaryActivity.md)。
2. 拖入一个 **添加键值对** 组件至流程中。
3. 配置 **添加键值对** 组件的属性。

    - 字典：输入变量面板中已定义的字典变量，如，`D`
    - 键/值：输入需要向字典变量中添加的键值对。如，`key3`、`value3`

4. 拖入一个 **写入日志** 组件至 **添加键值对** 组件的下方, 用于输出已添加的键值对。
5. 配置 **写入日志** 组件的属性。

    - 日志级别：输入日志级别，如，`Info`
    - 日志内容：输入日志内容，如，`D["key3"]`，表示输出 key3 键对应的的值。

6. 最终的流程如下图所示。

    ![流程图](https://docimages.blob.core.chinacloudapi.cn/images/Activities/addkeyvalue20210111.png)

7. 保存并运行流程。
8. 在输出面板中查看运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/addkeyvalueresult20210111.png)
