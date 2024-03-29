# 反序列化

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Deserialization.mp4"></video>

## 概述

将JSON字符串反序列化为.NET对象。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **JSON字符串** ：输入欲被反序列化为JSON数据。

### 输出

- **结果**：输入被反序列化后的对象；仅支持变量。

## 使用示例

**此流程执行逻辑**：将定义的变量`json字符串`反序列化为`json对象`输出。

![配置反序列化组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject3.png)

> **说明：**
>
> 若想了解更多关于**json**的内容，请参考网上的**[json教程](https://www.runoob.com/json/json-tutorial.html)**

## 常见问题

1. **Q：通用文字识别得到JSON，进行反序列化后，Object如何调用其中的Value值？**

    **A：** `Convert.ToString(jobj["data"]["result"][0])`

    ![反序列化](https://docimages.blob.core.chinacloudapi.cn/images/Activities/json20210825.png)