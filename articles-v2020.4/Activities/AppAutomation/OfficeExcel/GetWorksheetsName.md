# 获取所有工作表名

## 视频示例

## 概述

获取工作簿内所有工作表名称。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **工作表名称** ：工作簿内所有工作表名存储到此变量。可结合循环组件输出或使用工作表名

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **获取所有工作表名** 组件到 **打开/新建** 组件中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AutoFillRange1.png)

5. 拖拽 **循环操作（For Each）** 到 **打开/新建** 组件中，拖拽 **写入日志** 到 **循环操作（For Each）** 组件中，填入变量：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName2.png)

6. 运行成功后，日志打印所有 sheet 名称：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName3.png)
