# 插入工作表

## 视频示例

## 概述

在工作簿内插入指定的工作表。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **插入模式** ：包括两种模式：新建工作表，复制工作表。新建工作表模式指将在工作簿中创建一个新的工作表并插入到指定位置。复制工作表模式指将在工作簿中复制已有工作表副本并插入到指定位置。
- **插入位置** ：指定插入工作表的位置。例如“1”，即插入工作表的位置为第一个。当为空时，默认插入到最后；超过最大位置，则默认插入到最后
- **新工作表名称** ：欲插入的新工作表名
- **源工作表名** ：欲复制的工作表名

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **插入工作表** 组件到 **打开/新建** 组件中，插入模式选择复制工作表，插入位置 2，新工作表名称“sheetNew”，填写源工作表名称“sheet1”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertWorksheets1.png)

5. 运行成功后，打开 excel 查看，工作表“sheetNew”插入到第一个位置并且复制“sheet1”的内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertWorksheets2.png)
