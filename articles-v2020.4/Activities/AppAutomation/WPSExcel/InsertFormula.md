# 插入公式

## 视频示例

## 概述

向单元格插入公式，并填充公式运行后的结果

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：插入公式的目标单元格所属工作表。仅支持字符串变量和字符串
- **单元格** ：执行插入公式操作的目标单元格，支持区域。仅支持字符串变量和字符串
- **公式** ：插入的公式。支持两种写法：含公式名（例：SUM(A1, A2)），不含公式名（A1+A2）；两种写法均可省略等号。仅支持字符串变量和字符串

### 输出

- **执行结果** ：将公式执行结果存储在此变量

## 使用示例

1. 新建一个 Excel 文件，并在 Sheet1 的 A1-E1 单元格中分别填写数字 10，11，12，13，14:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps55.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **插入公式** 组件，分别填写工作表和单元格位置，以及公式内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps56.png)

4. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps57.png)
