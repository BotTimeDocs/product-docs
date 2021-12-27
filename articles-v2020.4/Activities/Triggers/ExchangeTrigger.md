# 邮件触发器(Exchange)

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/MailTriggerExchange.mp4"></video>

## 概述

邮件触发器（Exchange）用于监听Exchange服务器接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 服务器

- **Exchange版本** ：选择Exchange版本
- **服务器** ：输入被监听的服务器地址。

### 邮件

- **域名** ：输入被监听的域名。
- **邮箱地址** ：输入被监听的邮箱地址。
- **邮箱密码** ：输入被监听邮箱对应的密码。
- **共享账号** ：输入被监听的共享账号地址。

### 输出

- **新邮件** ：输出监听到的新邮件。仅支持System.Net.Mail.MailMessage变量

### 可选项

- **发件人** ：输入监听的邮件中发件人邮箱地址；支持多个，多个则以英文分号分隔；新邮件中包含其中一个发件人则视为满足触发条件。
- **附件** ：选择是否监听有附件的新邮件。
- **文件夹** ：输入被监听的邮箱文件夹（根据本机所安装Outlook语言版本而设置：例如英文版写 “inbox”, 中文版写 “收件箱”）；为空则监听整个收件箱。
  
  > **说明：**
  >
  > 以中文版为例：若监听子文件夹需填写 “收件箱\文件夹名称”，若只填写“收件箱”监听不到子文件夹邮件。
  
- **标题关键字** ：输入监听新邮件中包含的标题关键字；支持多个，多个则以英文分号分隔；新邮件中包含其中一个标题关键字则视为满足触发条件。
- **超时** ：输入超时时间，格式：时:分:秒。

## 使用示例

**此流程执行逻辑**：指定Exchange邮件服务器地址，自动监听接收新邮件。

![配置邮件触发器(Exchange)组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExchangeTrigger1.png)
