# 元素是否存在

## 视频示例

## 概述

验证输入的元素是否存在于指定的数组

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数组** ：指定被验证元素是否属于此数组
- **元素** ：输入欲验证的元素

### 输出

- **结果** ：输出Boolean校验结果

## 使用示例

1. 拖入**元素是否存在**组件，设置变量`数组`，变量类型为`String[]`，默认值`new string[]{"A","B","C"}`，设置Boolean变量`isexist`，**输入**数组变量`数组`，**输入**元素`"B"`，**输出**结果`isexist`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExistsInArrayActivity1.png)
2. 拖入**写入日志**组件，输入**日志内容**`isexist.ToString()`，`"B"`元素存在于此数组，打印结果为`True`：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExistsInArrayActivity2.png)
