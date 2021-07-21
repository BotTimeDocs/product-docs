# 文本转日期和时间

## 视频示例

## 概述

将文本转换为日期和时间。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **文本格式**：指定输入的文本格式（即，日期和时间格式），可手写。

### 输入

- **文本**：欲被转换为 DateTime 的字符串，可接变量。

### 输出

- **日期和时间**：被转换成的 DateTime 变量，仅可接变量。

## 使用示例

1. 拖入**文本转日期和时间**组件至流程。
2. 配置属性参数如下：
   ![操作样例](https://docimages.blob.core.chinacloudapi.cn/images/Activities/texttodatetime20201216.png)

    - 文本：输入需要转日期和时间格式的文本内容，如，"2020-12-16"
    - 文本格式：下拉选择输入的文本格式，如，"yyyy-mm-dd"
    - 日期和时间：自定义一个变量（DT），用于存放转换后的日期和时间格式，如，DT

3. 查看输出的变量值（即，最终转成的日期和时间的值），拖入一个**写入日志**组件至流程中，并配置该组件的输出样式，如，"文本转日期和时间的值为"+DT
   ![配置输出](https://docimages.blob.core.chinacloudapi.cn/images/Activities/outputdate20201216.png)
4. 在输出窗口中查看最终的输出值。  
   ![输出值](https://docimages.blob.core.chinacloudapi.cn/images/Activities/logscreen20201216.png)