# 移除对象

## 视频示例

## 概述

将指定的对象从目标集合中移除。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **对象**：输入欲被移除的对象。

### 输入输出

- **集合**：输出被移除对象后的集合结果。

## 使用示例

**前置必要条件**：已有一个添加对象的集合，参见[添加对象](../CollectionProcessing/AddToCollectionActivity.md)

**此流程执行逻辑**：将集合`集合List`中的指定对象`"A1"`移除，最终是否移除的结果保存至`isremoved`变量中。

![配置移除对象组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveFromCollectionActivity1.png)
