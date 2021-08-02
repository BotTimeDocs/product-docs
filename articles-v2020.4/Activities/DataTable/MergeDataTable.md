# 合并数据表

## 视频示例

## 概述

将数据表按照指定规则进行合并，并将合并后的结果更新到目标数据表中

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **目标数据表** ：将源数据表合并到此表，此表存储合并后的数据
- **源数据表** ：取此表数据合并到目标数据表，此表数据不会被更改
- **结构不同时** ：执行合并操作的两表结构不同时，取此项来执行合并操作实现数据的取舍

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 再拖入一次**搭建数据表**组件按步骤2创建数据表table2，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeDataTable20201225.png)

4. 拖入**合并数据表**组件和**预览数据表**组件，输入合并数据表的源数据表和目标数据表，例：table和table2，因为两个数据表结构不同，所以合并选项选择添加，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeDataTable2020122502.png)

5. 点击运行，查看运行结果，检查预览出的数据表是否是两个表添加合并的结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeDataTable2020122503.png)
