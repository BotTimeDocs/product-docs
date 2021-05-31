# 发送邮件(Exchange)

使用 Exchange 服务发送邮件

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 服务器

- **Exchange 版本** ：选择 Exchange 版本
- **服务器** ：发件人邮箱所属服务器地址。仅支持字符串变量和字符串

### 登录

- **域名** ：输入域名；若为空则使用默认域名。仅支持字符串变量和字符串
- **账号** ：输入登录到 Exchange 账号。仅支持字符串变量和字符串
- **密码** ：输入 Exchange 账号的密码。仅支持字符串变量和字符串

### 发件人

- **邮箱地址** ：输入发件人邮箱地址。仅支持字符串变量和字符串

### 收件人

- **收件人** ：邮件接收人邮箱地址。可写多个收件人，用分开分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串
- **抄送人** ：发送邮件时的抄送人邮箱地址。可写多个收件人，用分开分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串
- **密件抄送** ：发送邮件时的密件抄送人邮箱地址。可写多个收件人，用分开分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串

### 邮件

- **邮件主题** ：发送邮件的主题。仅支持字符串变量和字符串
- **邮件内容** ：发送邮件的正文内容。仅支持字符串变量和字符串
- **附件** ：发送邮件的附件。支持相对和绝对路径。可写多个附件地址，具体写法参考：new List <string>(){"文件 1 路径", "文件 2 路径"}
- **保存为草稿** ：将编辑好的邮件保存到发件人草稿箱，不执行发送操作
- **HTML 格式** ：说明邮件内容是否时 HTML 格式，若勾选后，则按照 HTML 格式处理邮件内容
- **重要性**：选择邮件的重要等级，包括正常、高、低。
- **请求送达回执**：勾选后，发送的邮件送达到指定邮箱后会自动发送回执。
- **请求已读回执**：勾选后，发送的邮件被读后自动发送回执。

### 转发

- **邮件** ：指定欲转发的邮件。仅支持 System.Net.Mail.MailMessage 变量

## 操作样例

1. 拖入 **发送邮件(Exchange)** 组件至项目流程中：
 ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendExchangeMail20201222.png)

2. 输入 Exchange 账号和密码字符串，例：“××@encootech.com”和“×××”，输入邮箱服务地址字符串，例：“https://××× service.outlook.cn/” ，输入收件人字符串，例：“××2@encootech.com”，输入邮件内容字符串，例：“云扩科技：发送邮件（Exchange）”，输入邮件主题字符串，例："发送邮件（Exchange）"，如下图所示：
 ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendExchangeMail2020122202.png)

3. 点击运行，查看运行结果，登录发件箱查看邮件是否发送成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendExchangeMail2020122203.png)