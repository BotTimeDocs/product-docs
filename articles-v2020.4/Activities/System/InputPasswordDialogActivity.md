# 输入密码

## 视频示例

## 概述

提供人机交互界面，弹框形式展现并且带有密码输入框，接收用户输入的密码值并可以输出输入的密码

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **标题** ：输入弹窗的标题。仅支持字符串变量和字符串
- **描述** ：输入弹窗中的描述信息，帮助用户进行输入密码的操作。仅支持字符串变量和字符串

### 输出

- **输入的密码** ：将输入的密码存储在此变量。仅支持字符串变量和字符串

## 使用示例

1. 拖入**输入密码**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-1.png)

2. 双击**输入密码**组件的空白处，配置属性参数：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-2.png)

3. 拖入**写入日志**组件到设计面板中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-3.png)

4. 保存并运行流程，输入密码“123456”，可以看到控制台打印出用户输入的密码值：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-4.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-5.png)