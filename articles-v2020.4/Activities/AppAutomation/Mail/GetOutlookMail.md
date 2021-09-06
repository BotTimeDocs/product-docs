# 获取邮件(Outlook)

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetOutlookMail.mp4"></video>

## 概述

获取本机 Outlook 账号中邮件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输出

- **邮件** ：将获取到的邮件存储在此变量，变量类型为 List <System.Net.Mail.MailMessage>;

### 邮件

- **邮箱地址** ：设置将要获取邮件的邮箱地址。
- **邮件文件夹** ：指定邮箱中的文件夹，若为中文版 Outlook 填写“收件箱”，英文版则填写 "inbox"; 若获取 inbox 下子级文件夹邮件，需使用 "\" 分隔，例如: "inbox\客户邮件"
- **获取封数** ：获取邮件的封数。默认为 1。

### 可选项

- **标记为已读** ：默认获取的邮件在 Outlook 中不标记为已读，勾选后则将获取的邮件标记为已读。
- **仅获取未读邮件** ：默认仅获取未读邮箱，若不勾选则获取所有状态邮件。
- **筛选** ：支持输入 JET / DASL query 语法检索过滤邮件，例如仅获取只读的邮件 query 为 "[UnRead] = True"，如果当前输入的 query 与其他属性选项有冲突，则优先使用其他属性选项值。具体写法参考：https://docs.microsoft.com/zh-cn/office/vba/outlook/how-to/search-and-filter/filtering-items

## 使用示例

**此流程执行逻辑**：获取 Outlook 服务账号中“收件箱”中的邮件。

![配置获取邮件(Outlook)组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122202.png)
