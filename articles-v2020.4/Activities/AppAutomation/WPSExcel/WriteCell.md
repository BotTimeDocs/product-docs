# 写入单元格

## 视频示例

## 概述

写入数据到指定单元格

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **单元格** ：写入数据的目标单元格地址。可输入单元格或区域，当输入区域时，则在指定区域每一个单元格内输入相同数据。仅支持字符串变量和字符串
- **工作表** ：写入数据的目标工作表。若指定工作表不存在则自动新建。仅支持字符串变量和字符串
- **数据** ：写入单元格内的数据。可传入&quot; 读取单元格&quot; 的输出变量，实现复制粘贴效果，同时保持复制源的数据格式。仅支持字符串变量和字符串

## 使用示例

1. 拖入 **打开/新建** 组件，勾选是否新建文件，再填入需要打开或者新建的 Excel 文件，并配置所需选项内容:

    ![1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps1.png)

2. 双击 **打开/新建** 组件，拖入 **写入单元格** 组件，设置工作表名称、单元格位置以及数据内容:

    ![2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps44.png)

3. 点击流程运行，观察运行结果:

    ![3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps45.png)
