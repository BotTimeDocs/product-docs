# 排序

## 视频示例

## 概述

对指定数据表的指定列进行排序，并将排序后的结果存储到输出数据表

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **列名** ：指定执行排序操作的列--通过列名定位。三个属性"数据列，列名，列索引"必三选一且互斥
- **列索引** ：指定执行排序操作的列--通过列索引定位。三个属性"数据列，列名，列索引"必三选一且互斥
- **排序方式** ：指定按照何种顺序进行排序。含两个值：升序，降序。默认升序
- **数据表** ：将对此数据表内的行数据进行判断，若不同行之间有完全相同的数据，则仅保留一行数据
- **数据表列** ：指定执行排序操作的列--通过DateColumn对象定位。三个属性"数据列，列名，列索引"必三选一且互斥

### 输出

- **数据表** ：将排序后的数据表保存到此变量。当此处为空或提供的变量名和原表相同时，默认在原表做更改；当此处值和原表不同时，将改变存入提供表内。（即，仅当需将改变存到新表时，需填充此项）

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateRow20201228.png)

3. 拖入**排序**组件和**预览数据表**组件，输入和输出都填入数据表变量，例：table，列名填入需要排序的列，例：“年龄”，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SortDataTable20201229.png)

4. 点击运行，查看运行结果，检查预览出的数据表是否按照“年龄”列升序排列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SortDataTable2020122902.png)

