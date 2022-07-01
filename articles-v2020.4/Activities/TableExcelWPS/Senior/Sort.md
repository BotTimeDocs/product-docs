# 排序

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Sort.mp4"></video>

## 概述

对某列进行升序或降序排序。

> **说明：**
>
> 该组件需在 Office Excel 的 **打开/新建** 组件内进行使用。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 可选项

- **开始行号** ：执行开始排序的行号。若为空，则默认从第一行开始执行排序。

### 输入

- **方式**：指定文本的排序方式。
    - **常规**：默认值。分别对数字和文本数据进行排序。
    - **文本作为数字型数据**：将文本作为数字型数据进行排序。
- **工作表** ：执行排序的目标工作表。
- **列号** ：对此列进行排序操作，支持数字或字母形式的列号，如，1、2、3、A、B、C等。
- **顺序** ：下拉框选择排序模式为升序或降序。

## 使用示例

**前置必要组件**：[打开/新建](../../TableExcelWPS/OpenExcel.md)

**此流程执行逻辑**：对指定工作表“Sheet2”中的第 1 列数据进行升序排序。

![配置排序组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Sort2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Sort3.png)
