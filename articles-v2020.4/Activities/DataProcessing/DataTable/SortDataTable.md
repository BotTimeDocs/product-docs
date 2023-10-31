# 排序

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SortDatatable.mp4"></video>

## 概述

对指定数据表的指定列进行排序，并将排序后的结果存储到输出数据表。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **列名** ：指定执行排序操作的列--通过列名定位。三个属性"数据列，列名，列索引"必三选一且互斥
- **列索引** ：指定执行排序操作的列--通过列索引定位。三个属性"数据列，列名，列索引"必三选一且互斥
- **排序方式** ：指定按照何种顺序进行排序。含两个值：升序，降序。默认升序
- **数据表** ：指定的数据表名称。
- **数据表列** ：指定执行排序操作的列--通过DateColumn对象定位。三个属性"数据列，列名，列索引"必三选一且互斥

### 输出

- **数据表** ：将排序后的数据表保存到此变量。当此处为空或提供的变量名和原表相同时，默认在原表做更改；当此处值和原表不同时，将改变存入提供表内。（即，仅当需将改变存到新表时，需填充此项）

## 使用示例

**前置必要组件**：已有一个已搭建的数据表，可参见 [搭建数据表](../../DataProcessing/DataTable/BuildDataTable.md)。

**此流程执行逻辑**：将数据表`table`中的`"年龄"`列进行升序排序。

![配置排序组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SortDataTable20201229.png)
