# 发送邮件(Exchange)

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SendExchangeMail.mp4"></video>

## 示例

使用 Exchange 服务发送邮件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 登录

- **密码** ：输入 Exchange 账号的密码。
- **域名** ：输入域名，若为空则使用默认域名。
- **账号** ：输入登录到 Exchange 账号。

### 发件人

- **邮箱地址** ：输入发件人邮箱地址。

### 服务器

- **Exchange 版本** ：选择 Exchange 版本
- **服务器** ：发件人邮箱所属服务器地址。如，“https://××× service.outlook.cn/”。

### 收件人

- **抄送人** ：发送邮件时的抄送人邮箱地址。可写多个收件人，用分号分割即可；例如：`user1@encootech.com; user2@encootech.com`。
- **密件抄送** ：发送邮件时的密件抄送人邮箱地址。可写多个收件人，用分号分割即可；例如：`user1@encootech.com; user2@encootech.com`。
- **收件人** ：邮件接收人邮箱地址。可写多个收件人，用分号分割即可；例如：`user1@encootech.com; user2@encootech.com`。

### 邮件

- **HTML 格式** ：说明邮件内容是否时 HTML 格式，若勾选后，则按照 HTML 格式处理邮件内容。
- **保存为草稿** ：将编辑好的邮件保存到发件人草稿箱，不执行发送操作。
- **附件** ：发送邮件的附件。支持相对和绝对路径。可写多个附件地址，具体写法参考：new List <string>(){"文件 1 路径", "文件 2 路径"}
- **请求送达回执**：勾选后，发送的邮件送达到指定邮箱后会自动发送回执。
- **请求已读回执**：勾选后，发送的邮件被读后自动发送回执。
- **邮件内容** ：发送邮件的正文内容。如，“云扩科技：发送邮件（Exchange）”。
- **邮件主题** ：发送邮件的主题。如，"发送邮件（Exchange）"
- **重要性**：选择邮件的重要等级，包括正常、高、低。

### 转发

- **邮件** ：指定欲转发的邮件，仅支持 System.Net.Mail.MailMessage 变量。

## 使用示例

**此流程执行逻辑**：使用Exchange服务，将邮件内容发送给指定的收件人。

![配置发送邮件(Exchange)组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendExchangeMail2020122202.png)
