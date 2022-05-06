# 资产管理

## 概述

资产通常表示可在不同自动化项目中使用的共享变量或凭据。它们允许您存储特定信息，以便RPA流程轻松访问。

**资产管理**页面用于创建新资产，并显示已创建的所有资产，您可以编辑或删除这些资产。

编辑器中使用的“**获取资产**”组件根据提供的**资产名称**向控制台请求有关特定资产的信息。可参见[获取资产](../../../Activities/Console/GetAssets.md)。

## 资产类型

资产分为四种类型：

- 字符串：仅存储字符串（无需添加双引号）。
- 整型：仅存储整数。
- 浮点型: 仅存储小数。
- 布尔型：支持值Ture或False。
- 账户凭证密码：包含机器人执行特定流程所需的用户名和密码，例如，SAP 或 SalesForce 的登录详细信息。

## 资产的权限

若需指定某一资产的数据权限，可单击“资产名称”进入资产详情页，对该资产配置其数据权限。

- 用户权限：指定某部门/用户对该资产的管理权限。
- 机器人权限：指定某部门/机器人对该资产的管理权限。
- API KEY 访问权限：指定某API接口对该资产的管理权限。