# 读取单元格

## 视频示例

## 概述

获取工作簿单元格内数据并可存储在变量中

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **单元格** ：目标单元格。仅支持字符串变量和字符串
- **工作表** ：目标单元格所在工作表。仅支持字符串变量和字符串

### 输出

- **数据** ：输出读取的目标单元格内数据

## 使用示例

1. 新建一个 Excel 文件，在 A1 处填入需要被读取的值:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps4.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **读取单元格** 组件至 **打开/新建** 组件中，填写工作表和单元格位置，在输出数据中写入变量来接收读取的内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps6.png)

4. 拖入 **写入日志** 组件，来显示读取单元格的内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps7.png)

5. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps8.png)