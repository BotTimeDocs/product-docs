# 隐藏工作表

## 视频示例

## 概述

隐藏工作簿内指定的工作表名称。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。
### 输入

- **工作表** ：指定隐藏的工作表名称。

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **隐藏工作表** 组件到 **打开/新建** 组件中，填写 sheet 名称“sheet2”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HideWorksheets1.png)

5. 运行成功后，打开 excel 查看，sheet2 已经被隐藏：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HideWorksheets2.png)
