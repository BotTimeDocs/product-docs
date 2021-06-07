# 发送邮件(Outlook)

使用本机 Outlook 中配置的邮箱账号发送邮件

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 发件人

- **共享邮箱地址** ：使用 Outlook 中共享邮箱地址作为发件人，执行发送邮件操作。仅支持字符串变量和字符串
- **邮箱地址** ：发件人邮箱地址。仅支持字符串变量和字符串。

   >**说明：**
   >
   >若“共享邮箱地址”有效且当前属性输入的邮箱地址有“共享邮箱地址”的权限，则发送后的邮件“发件人信息”显示共享邮箱信息；

### 收件人

- **收件人** ：邮件接收人邮箱地址。可写多个收件人，用分号分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串
- **抄送人** ：发送邮件时的抄送人邮箱地址。可写多个收件人，用分号分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串
- **密件抄送** ：发送邮件时的密件抄送人邮箱地址。可写多个收件人，用分号分割即可；例如：【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。仅支持字符串变量和字符串

### 邮件

- **邮件主题** ：发送邮件的主题。仅支持字符串变量和字符串
- **邮件内容** ：发送邮件的正文内容。仅支持字符串变量和字符串
- **附件** ：发送邮件的附件。支持相对和绝对路径。可写多个附件地址，具体写法参考：new List <string>(){"文件 1 路径", "文件 2 路径"}，也可以点击 "..." 在弹窗中选择文件后自动生成
- **保存为草稿** ：将编辑好的邮件保存到发件人草稿箱，不执行发送操作
- **HTML 格式** ：说明邮件内容是否时 HTML 格式，若勾选后，则按照 HTML 格式处理邮件内容
- **重要性**：选择邮件的重要等级，包括正常、高、低。
- **请求送达回执**：勾选后，发送的邮件送达到指定邮箱后会自动发送回执。
- **请求已读回执**：勾选后，发送的邮件被读后自动发送回执。

### 转发

- **邮件** ：输入将要转发的邮件；等同于在 outlook 选中一封邮件点击“转发”; 仅支持 System.Net.Mail.MailMessage 类型
  
## 常见问题

1. 某个程序正试图在 Outlook 中代表你发送电子邮件警告 <br>
   ![发送邮件 outlook](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sendoutlookmail20201204.png) <br>
   解决办法：参见 [官方解答](https://docs.microsoft.com/zh-cn/outlook/troubleshoot/security/a-program-is-trying-to-send-an-email-message-on-your-behalf)

## 操作样例

1. 拖入 **发送邮件(Outlook)** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendOutlookMail2020122201.png)

2. 输入发件邮箱地址字符串，例：“××@encootech.com”，输入收件人字符串，例：“××2@encootech.com”，点击选择附件按钮选择作为附件的文件，例：`new List <string>{"C:\\Desktop\\发票.png"}`，输入邮件内容字符串，例：“云扩科技：发送邮件（Outlook）”，输入邮件主题字符串，例："发送邮件（Outlook）"，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendOutlookMail2020122202.png)

3. 点击运行，查看运行结果，并打开 outlook 发件箱查看邮件是否发送成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendOutlookMail2020122203.png)