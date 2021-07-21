# 插入行/列

## 视频示例

## 概述

向指定工作表中插入任意行或列。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **插入模式** ：选择插入行/列
- **插入行/列数** ：欲插入行/列的数量。值为整型
- **工作表** ：指定将要插入行或列的工作表名称
- **起始位置** ：欲在工作表中插入行/列的起始位置

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertRowOrColumn1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **插入行/列** 组件到 **打开/新建** 组件中，输入插入行/列数，插入模式选择“插入行”，填写工作表名称和起始位置；插入列操作同插入行：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertRowOrColumn2.png)

5. 运行成功后，打开 excel 查看，在 sheet1 第 3 行插入空行 2 行：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertRowOrColumn3.png)
