# 排序

对某列进行排序，提供&quot; 升序，降序&quot; 两种排序模式。工作表内所有行数据随之改变

## 属性

## 视频示例

## 概述

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **开始行号** ：执行开始排序的行号。若为空则默认从第一行开始执行排序。仅支持整型变量和整型

### 输入

- **方式**：指定文本的排序方式。
    - **常规**：默认值。分别对数字和文本数据进行排序。
    - **文本作为数字型数据**：将文本作为数字型数据进行排序。
- **工作表** ：执行排序的目标工作表。仅支持字符串变量和字符串
- **列号** ：对此列进行排序操作。填入列索引（例：1，即对第一列进行排序）。仅支持整型变量和整型
- **顺序** ：下拉框选择排序模式为升序或降序

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Sort1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **排序** 到 **打开/新建** 组件中，填写 sheet 名称 "sheet2"，填写需要排序的列 1，填写开始的行 1：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Sort2.png)

5. 运行成功后打开 Excel 查看第 1 列从第 1 行开始已经按照升序排列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Sort3.png)
