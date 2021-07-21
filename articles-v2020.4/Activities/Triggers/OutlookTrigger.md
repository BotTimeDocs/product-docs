# 邮件触发器(Outlook)

## 视频示例

## 概述

邮件触发器（Outlook）用于监听Outlook邮箱接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **发件人** ：输入监听的邮件中发件人邮箱地址；支持多个，多个则以英文分号分隔；新邮件中包含其中一个发件人则视为满足触发条件；可接变量
- **附件** ：选择是否监听有附件的新邮件
- **文件夹** ：输入被监听的邮箱文件夹（根据本机所安装Outlook语言版本而设置：例如英文版写 “inbox”, 中文版写 “收件箱”）；为空则监听整个收件箱；可接变量。
  
  > **说明：**
  > 
  > 以中文版为例：若监听子文件夹需填写 “收件箱\文件夹名称”，若只填写“收件箱”监听不到子文件夹邮件。

- **标题关键字** ：输入监听新邮件中包含的标题关键字；支持多个，多个则以英文分号分隔；新邮件中包含其中一个标题关键字则视为满足触发条件；可接变量
- **超时** ：输入超时时间，格式：时:分:秒

### 邮件

- **邮箱地址** ：输入被监听Outlook中配置的邮箱地址；可接变量

### 输出

- **新邮件** ：输出监听到的新邮件。仅支持System.Net.Mail.MailMessage变量

## 使用示例

1. 安装配置完成Outlook软件后，拖入**邮件触发器(Outlook)**，新建变量`newmail`，变量类型为`MailMessage`，**输入**邮箱地址，**输出**新邮件`newmail`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OutlookTrigger1.png)
2. 拖入**写入日志**组件，打印邮件内容，输入**日志内容**`newmail.Body`，运行程序，在运行的过程中，往此邮箱中发送一封邮件，Outlook收到邮件后，触发器(Outlook)检测到新邮件，观察打印结果，打印此新增邮件的内容，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OutlookTrigger2.png)
