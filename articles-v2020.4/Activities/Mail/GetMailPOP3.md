# 获取邮件(POP3)

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetPOP3Mail.mp4"></video>

## 概述

使用 POP3 服务获取邮件，同时可使用代理。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 服务器

- **服务器** ：获取邮件的目标邮箱所属服务器地址。如，“`×××.outlook.cn`”。
- **端口号** ：获取目标邮箱邮件时所经端口号。如，995。
- **代理** ：获取邮件时若要使用代理，则填充此属性；格式为【服务器：端口号】。

### 输出

- **邮件** ：将获取到的邮件存储在此变量。变量类型为 List <System.Net.Mail.MailMessage>;

### 邮件

- **获取封数** ：获取邮件的封数，默认为 1。
- **密码** ：获取邮件所属目标邮箱的密码。如，“`××× password`”。
- **邮件内容格式**：按需下拉选择邮件内容显示的格式，支持纯文本、HTML格式等。
- **邮箱地址** ：获取此邮箱地址中的邮件。如，“`××@encootech.com`”。

### 可选项

- **安全连接** ：指定检测加密方法，默认为自动。
- **超时**：指定此组件的执行时间。若超出此时间，组件还未执行，会抛出错误。

## 使用示例

**此流程执行逻辑**：获取 POP3 服务账号中“收件箱”中的邮件。

![配置获取邮件(POP3)组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetMailPOP32020122302.png)
