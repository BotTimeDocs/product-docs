# 获取末列号

## 视频示例

## 概述

获取工作表或指定行有数据区域的最后一列列号

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：获取末列号操作所属工作表。仅支持字符串变量和字符串
- **行** ：获取末列号的所属行索引（例：1，即获取第一行的末列号）。当此项为空时，取整表数据区域最后一列列号。仅支持整型变量和整型

### 输出

- **末列号(数字)** ：输出获取的数字末列号。仅支持整型变量
- **末列号(字母)** ：输出获取的字母末列号。仅支持字符串变量

## 使用示例

1. 拖入 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入 **获取末列号** 组件至项目流程中，填写 sheet 名称，填写要获取的行号，新建变量 "colNum" 类型为 Int32 用来存放数字类型的行号。新建变量 "colNumS" 类型为 String 用来存放字符串类型的行号。使用写入日志组件打印数字类型的行号和字符串类型的行号：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLastColumn1.png)

4. 点击运行，运行成功。打印数字类型的行号和字符串类型的行号成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLastColumn2.png)
