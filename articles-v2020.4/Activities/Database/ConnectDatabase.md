# 连接数据库

## 视频示例

## 概述

连接到指定数据库。点击**配置向导**后可进行连接测试。组件执行结束后自动断开连接，所有数据库相关操作均需放置在此组件内且无需二次配置连接。

>**说明：**
>
> 如果您需要连接 DB2 数据库，请确保您已安装如下运行环境及扩展。
>
> - *Microsoft Visual C++ 2005 RunTime Pack*。如果未安装，您可以下载 [RunTimePack.zip](https://docimages.blob.core.chinacloudapi.cn/images/Studio/DataBase/RuntimePack.zip) 并安装。
> - 在编辑器的“开始 > 工具”页中，单击“DB2 扩展”进行安装。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **ConncetionString** ：用于与数据库建立连接。例如：MySQL连接字符串"Server=服务器地址;Database=DB名称;Port=端口号;Uid=uid;Pwd=password;"
- **ProviderName** ：连接的数据库类型。现支持五种：SQL Server, MySql, Oracle, DB2, Teradata

## 使用示例

**此流程执行逻辑**：根据“配置向导”配置与MySQL数据库建立连接。

![配置连接数据库组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db2.png)
