# 发送邮件(Outlook)

使用本机Outlook中配置的邮箱账号发送邮件

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 发件人

- **共享邮箱地址** ：使用Outlook中共享邮箱地址作为发件人，执行发送邮件操作。仅支持字符串变量和字符串
- **邮箱地址** ：发件人邮箱地址。仅支持字符串变量和字符串。注意：若“共享邮箱地址”有效且当前属性输入的邮箱地址有“共享邮箱地址”的权限，则发送后的邮件“发件人信息”显示共享邮箱信息；

### 收件人

- **收件人** ：邮件接收人邮箱地址。可写多个收件人，用分开分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串
- **抄送人** ：发送邮件时的抄送人邮箱地址。可写多个收件人，用分开分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串
- **密件抄送** ：发送邮件时的密件抄送人邮箱地址。可写多个收件人，用分开分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串

### 邮件

- **邮件主题** ：发送邮件的主题。仅支持字符串变量和字符串
- **邮件内容** ：发送邮件的正文内容。仅支持字符串变量和字符串
- **附件** ：发送邮件的附件。支持相对和绝对路径。可写多个附件地址，具体写法参考：new List<string>(){"文件1路径","文件2路径"}，也可以点击"..."在弹窗中选择文件后自动生成
- **保存为草稿** ：将编辑好的邮件保存到发件人草稿箱，不执行发送操作
- **HTML格式** ：说明邮件内容是否时HTML格式，若勾选后，则按照HTML格式处理邮件内容

### 转发

- **邮件** ：输入将要转发的邮件；等同于在outlook选中一封邮件点击“转发”; 仅支持System.Net.Mail.MailMessage类型
  
## 常见问题

1. 某个程序正试图在 Outlook 中代表你发送电子邮件警告<br>
   ![发送邮件outlook](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sendoutlookmail20201204.png)<br>
   解决办法：参见[官方解答](https://docs.microsoft.com/zh-cn/outlook/troubleshoot/security/a-program-is-trying-to-send-an-email-message-on-your-behalf)