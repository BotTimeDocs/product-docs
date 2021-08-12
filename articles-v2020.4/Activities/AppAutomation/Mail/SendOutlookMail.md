# 发送邮件(Outlook)

## 视频示例

## 概述

使用本机 Outlook 中配置的邮箱账号发送邮件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 发件人

- **共享邮箱地址** ：使用 Outlook 中共享邮箱地址作为发件人，执行发送邮件操作。
- **邮箱地址** ：发件人邮箱地址。如，“`××@encootech.com`”。

   >**说明：**
   >
   >若“共享邮箱地址”有效且当前属性输入的邮箱地址有“共享邮箱地址”的权限，则发送后的邮件“发件人信息”显示共享邮箱信息；

### 收件人

- **抄送人** ：发送邮件时的抄送人邮箱地址。可写多个收件人，用分号分割即可；例如：`user1@encootech.com; user2@encootech.com`。
- **密件抄送** ：发送邮件时的密件抄送人邮箱地址。可写多个收件人，用分号分割即可；例如：`user1@encootech.com; user2@encootech.com`。
- **收件人** ：邮件接收人邮箱地址。可写多个收件人，用分号分割即可；例如：`user1@encootech.com; user2@encootech.com`。

### 邮件

- **HTML 格式** ：说明邮件内容是否时 HTML 格式，若勾选后，则按照 HTML 格式处理邮件内容。
- **保存为草稿** ：将编辑好的邮件保存到发件人草稿箱，不执行发送操作。
- **附件** ：发送邮件的附件。支持相对和绝对路径。可写多个附件地址，具体写法参考：new List <string>(){"文件 1 路径", "文件 2 路径"}，也可以点击 "..." 在弹窗中选择文件后自动生成。
- **请求送达回执**：勾选后，发送的邮件送达到指定邮箱后会自动发送回执。
- **请求已读回执**：勾选后，发送的邮件被读后自动发送回执。
- **邮件内容** ：发送邮件的正文内容。如，“云扩科技：发送邮件（Outlook）”。
- **邮件主题** ：发送邮件的主题。例，"发送邮件（Outlook）"。
- **重要性**：选择邮件的重要等级，包括正常、高、低。

### 转发

- **邮件** ：输入将要转发的邮件；等同于在 outlook 选中一封邮件点击“转发”; 仅支持 System.Net.Mail.MailMessage 类型。

## 使用示例

**此流程执行逻辑**：使用Outlook服务，将邮件内容发送给指定的收件人。

![配置发送邮件(Outlook)组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendOutlookMail2020122202.png)

## 常见问题

1. 某个程序正试图在 Outlook 中代表你发送电子邮件警告 <br>

   ![发送邮件 outlook](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sendoutlookmail20201204.png)

   <br>

   解决办法：参见 [官方解答](https://docs.microsoft.com/zh-cn/outlook/troubleshoot/security/a-program-is-trying-to-send-an-email-message-on-your-behalf)
