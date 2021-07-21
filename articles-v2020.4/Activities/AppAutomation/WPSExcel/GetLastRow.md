# 获取末行号

## 视频示例

## 概述

获取工作表或指定列有数据区域的最后一行行号

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：获取末行号操作所属工作表。仅支持字符串变量和字符串
- **列号** ：获取末行号的所属列索引（例：1，即获取第一列的末行号）。当此项为空时，取整表数据区域最后一行行号。仅支持整型变量和整型

### 输出

- **末行号** ：将取到的末行号存储在此整型变量内。

## 使用示例

1. 新建一个 Excel 文件，在 A1: B8 处填入需要被读取的值:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps29.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **获取末列号** 组件至 **打开/新建** 组件中，并配置工作表名称和行号，输出的列号赋值给变量:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps37.png)

4. 拖入 **获取末行号** 组件至 **打开/新建** 组件中，并配置工作表名称和列号，输出的行号赋值给变量:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps38.png)

5. 拖入 **写入日志** 组件，来显示读取行号和列号的内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps39.png)

6. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps40.png)