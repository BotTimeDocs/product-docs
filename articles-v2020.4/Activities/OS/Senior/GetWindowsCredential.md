# 获取 Windows 凭据

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetWindowsCredentials.mp4"></video>

## 概述

获取本机 Windows 凭据管理器中 Windows 凭据分类中的普通凭据。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **凭据名** ：取此凭据名查找用户名和密码，并将结果保存到输出变量。

### 输出

- **用户名** ：将获取到的用户名保存到此变量。
- **密码** ：将获取到的密码保存到此变量。

## 使用示例

**前置必要步骤**：

![创建凭据](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-2.png)

**此流程执行逻辑**：根据在“控制面板 > 所有控制面板项 > 凭证管理器”中已创建的凭据，获取该凭据的用户名及密码信息。

![配置获取凭据组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-1.png)
