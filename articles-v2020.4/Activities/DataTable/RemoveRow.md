# 移除行

## 视频示例

## 概述

删除指定数据表的指定行，并自动保存同步其数据至指定数据表

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将移除此表的指定行
- **数据表行** ：移除数据表中的数据表行对象。和&quot;行索引&quot;属性两者互斥，只能且必需填入一项
- **行索引** ：移除数据表中行的行索引。和&quot;数据表行&quot;属性两者互斥，只能且必需填入一项。仅支持整型变量和整型

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 拖入**移除行**组件和**预览数据表**组件，输入数据表变量，例：table，输入数据表行，例：table.Rows[2]，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveRow20201228.png)

4. 点击运行，查看运行结果，检查预览出的数据表是否移除了第三行的值：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveRow2020122802.png)