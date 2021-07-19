# 序列化

## 视频示例

![序列化视频示例]()

## 概述

此组件可以将 .NET 对象序列化为 JSON 字符串。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **对象** ：用于被序列化的对象的变量。如，`json对象`。

### 输出

- **结果(JSON)** ：用于接收被序列化为 JSON 后数据的变量。如，`json字符串`。

## 使用示例

**此流程执行逻辑**：将 Json对象`JObject.Parse("{'名称':'云扩RPA','版本':1.0}")`转换成标准化Json字符串：

![配置项](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SerializeObject2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SerializeObject3.png)

> 若想了解更多关于 **json** 的内容，请参考网上的 **[json 教程](https://www.runoob.com/json/json-tutorial.html)**
