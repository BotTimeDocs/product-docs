# 合并单元格

## 视频示例

## 概述

对指定单元格区域进行合并操作。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：指定欲进行合并单元格操作所属工作表名称
- **区域** ：指定欲进行合并单元格区域

### 输出

- **合并值** ：合并后单元格的值。若合并单元格区域中只有一个值，则默认输出此唯一值；
若合并单元格区域中有多个值，则输出第一个非空单元格中的值

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **合并单元格** 和 **写入日志** 到 **打开/新建** 组件中，填写 sheet 名称 "sheet2"，填写合并的区域 "A1: A3"，新建 String 类型的变量 merge，配置在合并值中；把合并值配置到写入日志的内容中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells2.png)

5. 点击运行，运行后打开 Excel 查看单元格合并的结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells3.png)

6. 输出中打印合并后的标题：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells4.png)
