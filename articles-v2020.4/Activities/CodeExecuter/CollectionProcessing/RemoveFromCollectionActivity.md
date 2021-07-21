# 移除对象

## 视频示例

## 概述

将指定的对象从目标集合中移除

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **对象** ：输入欲被移除的对象

### 输入输出

- **集合** ：输出被移除对象后的集合结果

## 使用示例

1. 拖入**初始化集合**组件，设置变量`集合List`，变量类型为`List<String>`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InitializeCollectionActivity1.png)
2. 拖入**添加对象**组件，**输入**需要添加的对象`"A1"`，**输入/输出**`集合List`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddToCollectionActivity1.png)
3. 拖入**移除对象**组件，**新建**Boolean变量`isremoved`，**输入/输出**`集合List`，**输入**对象`"A1"`，**输出**结果`isremoved`，如下图所示：
    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveFromCollectionActivity1.png)
4. 拖入**写入日志**组件，输入**日志内容**`isremoved.ToString()`，打印结果移除成功`True`：
    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveFromCollectionActivity2.png)
