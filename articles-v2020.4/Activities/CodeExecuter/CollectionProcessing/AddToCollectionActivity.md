# 添加对象

## 视频示例

## 概述

将对象添加到指定集合

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **对象** ：输入欲添加至集合的对象

### 输入输出

- **集合** ：输出添加对象后的集合结果

## 使用示例

1. 拖入**初始化集合**组件，设置变量`集合List`，变量类型为`List<String>`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InitializeCollectionActivity1.png)
2. 拖入**添加对象**组件，**输入**需要添加的对象`"A1"`，**输入/输出**`集合List`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddToCollectionActivity1.png)
3. 拖入**写入日志**组件，打印`集合List`中的第一个内容，输入**日志内容**`集合List[0]`，打印结果`A1`，如下图所示：
 ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddToCollectionActivity2.png)
      