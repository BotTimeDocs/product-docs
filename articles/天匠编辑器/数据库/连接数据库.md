# 连接数据库

连接到指定数据库.点击&quot;配置向导&quot;后可进行连接测试。组件执行结束后自动断开连接，所有数据库相关操作均需放置在此组件内且无需二次配置连接

## 属性

输入

- **ConncetionString** ：用于与数据库建立连接。仅支持字符串变量和字符串
- **ProviderName** ：连接的数据库类型。现支持五种：SQL Server, MySql, Oracle, DB2, Teradata
