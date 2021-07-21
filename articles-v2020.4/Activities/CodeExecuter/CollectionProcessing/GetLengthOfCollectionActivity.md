# 获取集合长度

## 视频示例

## 概述

获取指定集合的长度

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **集合** ：指定目标集合

### 输出

- **长度** ：输出目标集合的长度；仅可接Int变量

## 使用示例

1. 拖入**初始化集合**组件，设置变量`集合List`，变量类型为`List<String>`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InitializeCollectionActivity1.png)
2. 拖入**添加对象**组件，**输入**需要添加的对象`"A1"`，**输入/输出**`集合List`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddToCollectionActivity1.png)
3. 拖入**获取集合长度**组件，新建变量`集合count`，**输入**变量`集合List`，**输出**长度变量`集合count`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfCollectionActivity1.png)
4. 拖入**写入日志**组件，打印`集合List`的长度，输入**日志内容**`集合count.ToString()`，打印结果为`1`：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfCollectionActivity2.png)
