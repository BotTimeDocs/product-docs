# 元素是否存在

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ElementIsNotExist.mp4"></video>

## 概述

验证输入的元素是否存在于指定的数组。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **数组** ：指定被验证元素是否属于此数组。
- **元素** ：输入欲验证的元素。

### 输出

- **结果**：输出Boolean校验结果。

## 使用示例

**此流程执行逻辑**：判断`"B"`元素是否存在于指定的数组`new string[]{"A","B","C"}`中，返回的结果存储在`isexist`变量中。

![配置元素是否存在组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExistsInArrayActivity1.png)
