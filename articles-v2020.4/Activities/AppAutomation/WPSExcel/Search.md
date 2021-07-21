# 查找

## 视频示例

## 概述

在特定单元格区域内查找给定值，并返回第一个查找到的单元格地址

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **查找内容** ：取此值进行查找。仅支持字符串变量和字符串
- **工作表** ：执行查找操作的目标工作表。仅支持字符串变量和字符串
- **区域** ：查找操作的目标单元格区域。为空时，默认查找全表

### 输出

- **单元格地址** ：将查找到的第一个单元格地址存储在此变量。仅支持字符串变量和字符串

## 使用示例

1. 新建一个 Excel 文件，在 A1: B7 处填入需要被读取的值:

    ![1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps9.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:

    ![2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **查找** 组件至 **打开/新建** 组件中，填写工作表和起始单元格位置以及需要查找的内容，将输出的单元格地址赋值给变量:

    ![3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps17.png)

4. 拖入 **写入日志** 组件，来显示需要获取单元格地址的内容:

    ![4](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps18.png)

5. 点击流程运行，观察运行结果:

    ![5](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps19.png)
