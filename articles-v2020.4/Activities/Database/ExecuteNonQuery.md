# 执行语句（Non Query）

## 视频示例

## 概述

需在&quot;连接数据库&quot;和&quot;执行事务&quot;内使用，无需二次配置连接。执行指定的Non Query语句，例如UPDATE, INSERT, DELETE，并返回语句执行后受影响的作用行数。若执行其他非Non Query 语句，返回-1

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **超时**：超时时间（时分秒），默认超时时间：00:00:30，可接变量。

### 输入

- **Sql语句** ：要执行的Non Query语句。仅支持字符串变量和字符串

### 输出

- **作用行数** ：将语句执行后受影响的作用行数存储到此变量。仅支持整型变量和整型

## 使用示例

1. 拖入**连接数据库**组件，选择当前所需访问数据库类型，再配置连接数据库字符串:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db1.png)

2. 双击**连接数据库**组件，点击"配置向导"按钮，如果已配置数据库字符串信息以及选择了目标数据库类型，则点击"测试连接"按钮，测试成功会提示绿色对勾，反之则失败，需要更新连接数据库字符串内容，确保无误之后重新测试连接，点击"确认"退出配置界面:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db2.png)

3. 拖入**执行语句**组件，配置sql语句:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db7.png)

4. 点击流程运行，并观察结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db8.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db9.png)
