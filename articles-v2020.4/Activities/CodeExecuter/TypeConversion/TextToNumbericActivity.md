# 文本转数值

## 视频示例

## 概述

实现将文本转换为数值。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **文本**：欲被转换为数值的字符串，可接变量。

### 输出

- **数值**：被转换成的数值变量，仅可接变量。
  
  >**说明：**
  >
  >该属性变量的参数类型仅支持Int、Double、Float、Decimal。

## 使用示例

1. 拖入一个**文本转数值**组件至流程中。
2. 配置**文本转数值**组件的属性。

    ![配置属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/texttonum20210104.png)

    - 文本：输入需要转换为数值的字符串，如，`"123.56"`
    - 数值：输入被转换为数值的变量，如，`S`

3. 在**文本转数值**组件下方，拖入一个**写入日志**组件，用于将文本转换成的数值的值进行输出查看。
4. 双击**写入日志**组件的空白处，配置属性。

    - 日志级别：下拉选择日志级别，如，`Info`
    - 日志内容：输入需要输出的日志内容，如，`"文本转数值为："+S`

5. 保存并运行流程。
6. 在编辑器的输出面板中查看运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/texttonumresult20210104.png)