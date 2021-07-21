# 写入行/列数据

## 视频示例

## 概述

横向或纵向写入数据到工作表中，支持自定义起始单元格地址执行写入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：写入数据的目标工作表。若指定工作表不存在则自动新建。仅支持字符串变量和字符串
- **起始单元格** ：写入数据的开始单元格地址。仅支持字符串变量和字符串
- **数据** ：写入工作表内的 IEnumerable\&lt; Object\&gt; 数据。可输入空格
- **写入行/列** ：写入数据的模式选择（横向写入数据或纵向写入数据）。选择&quot; 横向写入数据&quot; 后，则取用户指定的起始单元格地址，开始横向写入数据；选择&quot; 纵向写入数据&quot; 后，则取用户指定的起始单元格地址，开始纵向写入数据

## 使用示例

1. 拖入 **打开/新建** 组件，勾选是否新建文件，再填入需要打开或者新建的 Excel 文件，并配置所需选项内容:

    ![1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps1.png)

2. 双击 **打开/新建** 组件，拖入 2 个 **写入行/列数据** 组件，分别配置工作表名称、起始单元格位置、数据内容以及分别设置写入方式为横向写入数据和纵向写入数据:

    ![2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps51.png)

3. 点击流程运行，观察运行结果:

    ![3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps52.png)
