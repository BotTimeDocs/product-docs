# 对象是否存在

## 视频示例

## 概述

验证输入的对象是否存在于指定的集合

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **对象** ：输入欲验证的对象
- **集合** ：指定被验证对象是否属于此集合

### 输出

- **结果** ：输出Boolean校验结果

## 使用示例

1. 拖入**初始化集合**组件，设置变量`集合List`，变量类型为`List<String>`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InitializeCollectionActivity1.png)
2. 拖入**添加对象**组件，**输入**需要添加的对象`"A1"`，**输入/输出**`集合List`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddToCollectionActivity1.png)
3. 拖入**对象是否存在**组件，**新建**Boolean变量`isexist`，**输入/输出**`集合List`，**输入**对象`"A1"`，**输出**结果`isexist`，如下图所示：
    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExistsInCollectionActivity1.png)
4. 拖入**写入日志**组件，输入**日志内容**`isexist.ToString()`，打印结果对象存在`True`：
    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExistsInCollectionActivity2.png)
