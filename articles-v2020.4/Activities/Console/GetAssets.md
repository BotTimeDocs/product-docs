# 获取资产

## 视频示例

## 概述

可实现获取企业版控制台数据中心设置的资产。在编辑器或机器人运行时基于当前激活信息的控制台权限。
仅支持企业版。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **资源组/部门** ：输入或从下拉列表选择资源组。支持字符串变量或字符串
- **资产名称** ：输入或从下拉列表选择资产名称。支持字符串变量或字符串

### 输出

- **值** ：输出资产的值。仅支持变量。注意：变量类型依赖于所获取资产在控制台设置的值类型，例如获取凭证类资产，变量类型应为 Encoo.DataType.Credential；可使用Credential.UserName和Credential.Password获取用户名和密码

## 使用示例

1. 拖入**获取资产**组件至项目流程中，并设置变量result(String)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_1.png)

2. 双击打开获取资产，选择资源组和资源名称，在输出中添加变量result,如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_2.png)

3. 点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_3.png)

   >**说明：**
   >
   >组件需要私有化部署，控制端设置如下图所示：

   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_4.png)
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_5.png)
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_6.png)
