# 搭建数据表

## 视频示例

## 概述

按照自定义结构生成一个新的数据表。通过&quot;数据表搭建器&quot;，可以自定义列信息，并可同步预览定义的列并编辑行值

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **数据表** ：将搭建的数据表存储在此变量

## 数据表搭建器

界面化搭建数据表

- **列信息** ：增加、修改或移动列信息
  - 列名：数据表的列名
  - 数据类型：目前仅支持String、Int和Boolean类型
  - 默认值：当前列的默认值
  - 值可为空：是否可为空，默认可为空
  - 整型自动加一：若列类型为整型是否自动加一
  - 最大长度：最大支持长度，可为空

- **编辑行值** ：对添加的列增加行内容

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 拖入**预览数据表**组件并填入上面已经搭建好的数据表变量table：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122403.png)

4. 点击运行，查看运行结果，检查预览出的数据表与搭建的数据表是否一致：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122404.png)
