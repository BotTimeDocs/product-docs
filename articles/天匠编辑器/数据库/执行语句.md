# 执行语句（Non Query）

需在&quot;连接数据库&quot;和&quot;执行事务&quot;内使用，无需二次配置连接。执行指定的Non Query语句，例如UPDATE, INSERT, DELETE，并返回语句执行后受影响的作用行数。若执行其他非Non Query 语句，返回-1

## 属性

输入

- **Sql语句** ：要执行的Non Query语句。仅支持字符串变量和字符串

输出

- **作用行数** ：将语句执行后受影响的作用行数存储到此变量。仅支持整形变量和整形
