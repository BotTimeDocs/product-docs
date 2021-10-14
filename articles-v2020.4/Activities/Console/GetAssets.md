# 获取资产

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetAssets.mp4"></video>

## 概述

可实现获取企业版控制台数据中心设置的资产。在编辑器或机器人运行时基于当前激活信息的控制台权限。

>**说明：**
>
>该功能仅在企业版控制台中支持。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **资源组/部门** ：输入或从下拉列表选择资源组。
- **资产名称** ：输入或从下拉列表选择资产名称。

### 输出

- **值**：输出资产的值。仅支持变量。

   >**注意：**
   >
   >变量类型依赖于所获取资产在控制台设置的值类型，例如,获取凭证类资产，变量类型应为 Encoo.DataType.Credential；可使用Credential.UserName和Credential.Password获取用户名和密码。

## 使用示例

**前置必要条件**：在控制台中的“资产管理”中已创建资产。
**此流程执行逻辑**：获取指定的部门`"默认资源组"`下的资产`"测试字符串"`，结果保存至`result`变量中。

![配置获取资产组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_3.png)
