# 登录应用

## 视频示例

## 概述

实现打开SAP Logon 指定连接，并输入客户端、用户、口令登录连接。

> **说明：**
>
> 本功能仅在云扩企业版编辑器中支持。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **SAP Logon路径** ：SAP Logon的安装路径。
- **连接名** ：指定要登录的连接名 （Connection Name）。
  
  ![连接名样例](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connectionname20210325.png)

- **客户端** ：登录连接界面时要输入的客户端 （Client)。仅支持字符串变量和字符串

  ![客户端名样例](https://docimages.blob.core.chinacloudapi.cn/images/Activities/client20210325.png)

- **用户** ：登录连接界面时要输入的用户 （User)。
- **口令** ：登录连接界面时要输入的口令 （Password)。
- **多登录时** ：含三个值：继续此登录，保持同用户的其他连接；继续此登录，停止同用户的其他连接；停止此次登录。

## 使用示例

**此流程执行逻辑**：当有多登录时，停止此次登录SAP应用。

![配置登录应用组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SAPlogin-1.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SAPlogin-2.png)
