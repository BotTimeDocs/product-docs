# 读取行/列数据

## 视频示例

## 概述

读取指定工作表中的某一列或某一行，将读取到的内容保存在数组中并可输出

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **读取行/列** ：  指定组件操作为读取行或者为读取列。该选项为下拉选框（行，列），默认为行
- **工作表** ： 读取的目标行或列所在的工作表。仅支持字符串变量和字符串
- **起始单元格** ：  读取行或列时的起始单元格。将从此单元格开始，结合“读取行/列”属性所选择的行或列，来横向或者竖向读取数据。仅支持字符串变量和字符串

### 输出

- **数据** ： 输出数组类型的数据

## 使用示例

1. 新建一个 Excel 文件，在 A1: B7 处填入需要被读取的值:

    ![1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps9.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:

    ![2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **读取行/列数据** 组件至 **打开/新建** 组件中，填写工作表和起始单元格位置，在右侧配置输入中选择读取行，在输出数据中写入变量来接收读取的内容:

    ![3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps13.png)

4. 拖入另外一个 **读取行/列数据** 组件至 **打开/新建** 组件中，填写工作表和起始单元格位置，在右侧配置输入中选择读取列，在输出数据中写入变量来接收读取的内容:

    ![4](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps14.png)

5. 拖入 **写入日志** 组件，来显示需要获取的行和列的内容:

    ![5](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps15.png)

6. 点击流程运行，观察运行结果:

    ![6](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps16.png)
