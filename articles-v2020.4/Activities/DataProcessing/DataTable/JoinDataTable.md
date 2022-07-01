# 联结数据表

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ConnectDatatable.mp4"></video>

## 概述

根据联结条件，将两个数据表联结到一起，并将结果存储到输出输出数据表变量。提供四种联结条件：全连接，内连接，左连接，右连接。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **联结配置** ：点击右侧的按钮，将弹出联结配置窗口。在此窗口可以进行联结条件的设置。

### 输出

- **数据表**：将联结两表后的结果保存到此变量。

## 使用示例

**前置必要组件**：已有一个已搭建的数据表，可参见 [搭建数据表](../../DataProcessing/DataTable/BuildDataTable.md)。

**此流程执行逻辑**：将数据表 1 `table` 和数据表 2 `table2` 中的 `姓名` 字段以左连接的方式关联起来。

![配置联结数据表组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/JoinDataTable2020122502.png)
