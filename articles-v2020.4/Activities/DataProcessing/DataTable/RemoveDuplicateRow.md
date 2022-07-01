# 移除重复行

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/RemoveDuplicateRows.mp4"></video>

## 概述

删除指定数据表中的重复行，仅保留一行且保留行索引最小的行。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将对此数据表内的行数据进行判断，若不同行之间有完全相同的数据，则仅保留一行数据。

### 输出

- **数据表** ：将移除重复行后的数据表保存到此变量。当此处为空或提供的变量名和原表相同时，默认在原表做更改；当此处值和原表不同时，将改变存入提供表内（即，仅当需将改变存到新表时，需填充此项）。

## 使用示例

**前置必要组件**：已有一个已搭建的数据表，可参见 [搭建数据表](../../DataProcessing/DataTable/BuildDataTable.md)。

**此流程执行逻辑**：将数据表`table`中的重复行给去掉，相同的数据只保留一行数据。

![配置移除重复行组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateRow2020122802.png)
