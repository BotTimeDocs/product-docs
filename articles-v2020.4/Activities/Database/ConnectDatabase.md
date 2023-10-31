# 连接数据库

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ConnectDatabase.mp4"> </video>

## 概述

连接到指定数据库。点击 **配置向导** 后可进行连接测试。组件执行结束后自动断开连接，所有数据库相关操作均需放置在此组件内且无需二次配置连接。

> **说明：**
>
> 如果您需要连接 DB2 数据库，请确保您已安装如下运行环境及扩展。
>
> - *Microsoft Visual C++ 2005 RunTime Pack*。如果未安装，您可以下载 [RunTimePack.zip](https://docimages.blob.core.chinacloudapi.cn/images/Studio/DataBase/RuntimePack.zip) 并安装。
> - 在编辑器的“开始 > 工具”页中，单击“DB2 扩展”进行安装。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。 

### 输入

- **ConncetionString** ：用于与数据库建立连接。例如：MySQL 连接字符串 "Server = 服务器地址; Database = DB 名称; Port = 端口号; Uid = uid; Pwd = password;"
- **ProviderName** ：连接的数据库类型。现支持六种：SQL Server, MySql, Oracle, DB2, Teradata，PostgreSQL

## 使用示例

**此流程执行逻辑**：根据“配置向导”配置与 MySQL 数据库建立连接。

![配置连接数据库组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db2.png)

## 常见问题

1. **Q：Oracle 的数据库连接字符串格式是什么？**

    **A：** `"Data Source=(DESCRIPTION=(ADDRESS=(PROTOCOL=TCP)(HOST=192.168.161.150)(PORT=1521))(CONNECT_DATA=(SERVICE_NAME=orcl)));Persist Security Info=True;User ID=system;Password=sasa;"`

2. **Q：MySQL 的数据库连接字符串格式是什么？**

    **A：** `"Server=localhost;Port=3306;Database=nuget1;Uid=root;Pwd=root;"`

3. **Q：SQL Server 的数据库连接字符串格式是什么？**

    **A：** `"Data Source =DESKTOP-L7GL8TM;Initial Catalog =Northwind1;User Id =sa;Password =sasa;"`

4. **Q：Teradata 的数据库连接字符串格式是什么？**

    **A：** `"Data Source=localhost;User Id=sa;Password=sasa;"`

5. **Q：DB2 的数据库连接字符串格式是什么？**

    **A：** `"Server=127.0.0.1:50000;DataBase=Demo;UID= db2admin;PWD=sasa;"`

6. **Q：PostgreSQL 的数据库连接字符串格式是什么？**

    **A：** `"User ID=postgres;Password=123456;Host=127.0.0.1;Port=5432;Database=postgres;Pooling=true"`

7. **Q：连接DB2数据库时无法加载DLL“db2app.dll”，找不到指定模块(异常来自HRESULT:0x8007007E)**

    **A：**  按照如下步骤排查：

    a. 确认IBM DB2扩展是否已安装，若已更新过编辑器或机器人，则需要重新[安装IBM DB2扩展](./../../Studio/Extensions/ChromeExtension.md)。
    b. 确认是否安装*Microsoft Visual C++ 2005 RunTime Pack*，若未安装，则需按上文进行安装。
    c. 若以上步骤仍未解决，则需检查Windows 系统版本，是否是Windows Embedded Standard，若是，根据系统是64位系统还是32位系统下载安装
    - x64下载安装：https://share.weiyun.com/FFxPWka7
    - x86下载安装：https://share.weiyun.com/DBAnBZBe
