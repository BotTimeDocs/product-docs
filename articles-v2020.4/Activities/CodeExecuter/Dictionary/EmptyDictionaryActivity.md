# 清空字典

## 视频示例

## 概述

对已在变量面板创建的字典（Dictionary <TKey,TValue>）中的内容进行清空，即，移除所有的键和值。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入/输出

- **字典**：在变量面板中定义的字典对象，仅可接变量。

## 使用示例

1. 拖入一个 **初始化字典** 组件至流程中，具体属性配置参见 [初始化字典](CodeExecuter/../InitializeDictionaryActivity.md)。
2. 拖入一个 **添加键值对** 组件至流程中。
3. 配置 **添加键值对** 组件的属性。

    - 字典：输入变量面板中已定义的字典变量，如，`D`
    - 键/值：输入需要向字典变量中添加的键值对。如，`key3`、`value3`

4. 在 **添加键值对** 组件下方，拖入一个 **清空字典** 组件。
5. 配置 **清空字典** 组件的属性。

    - 字典：输入需要清空的字典变量，如，`D`

6. 完整的流程图如下。

    ![完整流程](https://docimages.blob.core.chinacloudapi.cn/images/Activities/emptydictionary20210112.png)

7. 保存并运行流程。
