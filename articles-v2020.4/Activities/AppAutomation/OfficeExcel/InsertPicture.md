# 插入图片

## 视频示例

## 概述

指定单元格插入图片

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **高度(像素)** ：输入被插入图片的高度，单位为像素，为空则使用图片原高度。仅支持 Float 变量和字符串
- **宽度(像素)** ：输入被插入图片的宽度，单位为像素，为空则使用图片原高度。仅支持 Float 变量和字符串

### 输入

- **单元格** ：被插入图片的目标单元格，支持区域。仅支持字符串变量和字符串
- **工作表** ：插入图片的目标单元格所属工作表。仅支持字符串变量和字符串
- **图片路径** ：指定插入图片的路径。仅支持字符串变量和字符串

## 使用示例

1. 新建一个 Excel 文件，存放在本地。

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **插入图片** 到 **打开/新建** 组件中，填写工作表名称，单元格名称和图片路径：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertPic1.png)

5. 运行成功后，sheet1 的 B2 中插入图片：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertPic2.png)
