# 去重

## 视频示例

## 概述

对指定工作表区域去除重复值, 保留第一非空行数据，删除剩余行内容。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：执行去重操作的目标工作表。仅支持字符串变量和字符串
- **区域** ：欲去重的单元格区域。

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateCells1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **去重** 到 **打开/新建** 组件中，填写 sheet 名称 "sheet2"，填写去重区域：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateCells2.png)

5. 运行成功后，在区域内删除重复的单元格内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateCells3.png)