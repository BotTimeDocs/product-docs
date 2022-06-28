# 对象是否存在

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ObjectIsNotExist.mp4"></video>

## 概述

验证输入的对象是否存在于指定的集合。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **对象** ：输入欲验证的对象。
- **集合** ：指定被验证对象是否属于此集合。

### 输出

- **结果**：输出Boolean校验结果。

## 使用示例

**前置必要条件**：已有一个添加对象的集合，参见[添加对象](../CollectionProcessing/AddToCollectionActivity.md)

**此流程执行逻辑**：判断对象`"A1"`在集合`集合List`中是否存在，返回结果存储在`isexist`变量中。

![配置对象是否存在组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExistsInCollectionActivity1.png)
