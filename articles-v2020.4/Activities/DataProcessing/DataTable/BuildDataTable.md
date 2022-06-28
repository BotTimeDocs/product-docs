# 搭建数据表

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/BuildDataTable.mp4"></video>

## 概述

按照自定义结构生成一个新的数据表。通过“数据表搭建器”，可以自定义列信息，并可同步预览定义的列并编辑行值。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **数据表**：将搭建的数据表存储在此变量。

## 数据表搭建器

界面化搭建数据表

- **列信息** ：增加、修改或移动列信息
  - 列名：数据表的列名
  - 数据类型：目前仅支持 String、Int 和 Boolean 类型
  - 默认值：当前列的默认值
  - 值可为空：是否可为空，默认可为空
  - 整型自动加一：若列类型为整型是否自动加一
  - 最大长度：最大支持长度，可为空

- **编辑行值** ：对添加的列增加行内容

## 使用示例

**此流程执行逻辑**：搭建一个数据表，保存至 `table` 变量中。

![配置搭建数据表组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)
