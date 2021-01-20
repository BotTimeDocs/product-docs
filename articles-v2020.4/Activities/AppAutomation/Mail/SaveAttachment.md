# 保存附件

将邮件中的附件保存到指定位置

## 属性

### 基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **邮件** ：取此邮件变量中的附件，执行保存操作
- **文件夹路径** ：附件保存位置。若出现同名文件则会报错；支持相对和绝对路径；路径不存在则自动新建。仅支持字符串变量和字符串

## 操作样例

1. 拖入 **获取邮件(Outlook)** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail20201222.png)

2. 输入 List <MailMessage> 类型的变量到邮件，例如：mail，输入邮件文件夹字符串，例：“收件箱”，输入邮件地址字符串，例：“××@encootech.com”，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122202.png)

3. 拖入 **保存附件** 和 **写入日志** 组件，输入 **保存附件** 的邮件，因为 **获取邮件(Outlook)** 的输出邮件是一个 List，所以这边输入的变量类型是 MailMessage，可以取 maillist 的第一个元素，例：mail [0]，输入文件夹路径，例：“C:\\云扩科技”，输入 **写入日志** 的日志内容，打印出获取的第一个邮件的内容，例：mail [0].Body.ToString()，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122203.png)

4. 点击运行，查看运行结果，检查获取附件和写入日志的邮件内容是否正确：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122204.png)