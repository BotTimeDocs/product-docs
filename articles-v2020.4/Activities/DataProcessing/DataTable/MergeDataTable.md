# 合并数据表

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/MergeDataTable.mp4"></video>

## 概述

将数据表按照指定规则进行合并，并将合并后的结果更新到目标数据表中。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **目标数据表** ：将源数据表合并到此表，此表存储合并后的数据。
- **源数据表** ：取此表数据合并到目标数据表，此表数据不会被更改。
- **结构不同时** ：执行合并操作的两表结构不同时，取此项来执行合并操作实现数据的取舍：

    选择“错误”：组件报错；</br>
    选择“忽略”：忽略不同；</br>
    选择“添加”：在表后追加。

## 使用示例

**前置必要条件**：已有两个已搭建的数据表，可参见 [搭建数据表](../../DataProcessing/DataTable/BuildDataTable.md)。

**此流程执行逻辑**：将源数据表 `table` 与目标数据表 `table2` 进行合并。

![配置合并数据表组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeDataTable2020122502.png)

## 常见问题

1. **Q：使用“合并数据表”组件时，报错：“[错误]目标表缺少列Colunm-0的定义”。**

    **A：** 两个数据表结构不一样，选择结构不同时的选项可检查数据源。
