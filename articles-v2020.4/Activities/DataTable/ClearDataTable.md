# 清空数据表

## 视频示例

## 概述

将数据表清空。原有结构将保留，仅清空数据

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：被执行清空操作的数据表

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 拖入**清空数据表**组件和**预览数据表**组件并给这两个组件填入上面已经搭建好的数据表变量table：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/EmptyDataTable20201225.png)

4. 点击运行，查看运行结果，检查预览出的数据表是否被清空：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/EmptyDataTable2020122502.png)

