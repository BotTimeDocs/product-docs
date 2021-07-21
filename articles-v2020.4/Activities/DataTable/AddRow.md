# 添加数据行

## 视频示例

## 概述

向数据表中添加一行数据，并自动保存同步至指定数据表

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将数据行添加到此表
- **数组** ：添加到数据表的数组。数组内的数据类型应和数据表中对应列的类型一致。和&quot;数据表行&quot;属性两者互斥，只能且必需填入一项
- **数据表行** ：添加到数据表的数据表行对象。和&quot;数组&quot;属性两者互斥，只能且必需填入一项

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 拖入**添加数据行**组件和**预览数据表**组件，输入数据表变量，例：table，创建类object[]类型的变量并设置初始化值来传递添加的数据行数组数据，例：addrow new object[]{"David","50","男"}，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddRow20201228.png)

4. 点击运行，查看运行结果，检查预览出的数据表是否增加的是addrow这一行数据：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddRow2020122802.png)
