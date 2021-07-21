# 获取 Windows 凭据

## 视频示例

## 概述

获取本机 Windows 凭据管理器中 Windows 凭据分类中的普通凭据。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **凭据名** ：取此凭据名查找用户名和密码，并将结果保存到输出变量。仅支持字符串变量和字符串

### 输出

- **用户名** ：将获取到的用户名保存到此变量。仅支持字符串变量和字符串
- **密码** ：将获取到的密码保存到此变量。仅支持字符串变量和字符串

## 使用示例

1. 拖入 **获取 Windows 凭据** 组件到设计面板，设置凭据名 "test01"，设置变量“pwd”，“userName”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-1.png)

2. 在电脑凭据管理器里新建一个普通凭据，凭据名：“test01”，用户名：“shirley”，密码：“123456”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-2.png)

3. 拖入 **写入日志** 组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-3.png)

4. 运行流程，控制台输出根据凭据名查找的用户名和密码：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-4.png)
