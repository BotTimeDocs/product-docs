# 获取邮件(Outlook)

获取本机 Outlook 账号中邮件

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 邮件

- **邮箱地址** ：设置将要获取邮件的邮箱地址。仅支持字符串变量和字符串
- **邮件文件夹** ：指定邮箱中的文件夹，若为中文版 Outlook 填写“收件箱”，英文版则填写 "inbox"; 若获取 inbox 下子级文件夹邮件，需使用 "/" 分隔，例如: "inbox/客户邮件"
- **获取封数** ：获取邮件的封数。默认为 1

### 可选项

- **标记为已读** ：默认获取的邮件在 Outlook 中不标记为已读，勾选后则将获取的邮件标记为已读
- **仅获取未读邮件** ：默认仅获取未读邮箱，若不勾选则获取所有状态邮件
- **筛选** ：支持输入 JET / DASL query 语法检索过滤邮件，例如仅获取只读的邮件 query 为 "[UnRead] = True"，如果当前输入的 query 与其他属性选项有冲突，则优先使用其他属性选项值。具体写法参考：https://docs.microsoft.com/zh-cn/office/vba/outlook/how-to/search-and-filter/filtering-items

### 输出

- **邮件** ：将获取到的邮件存储在此变量

## 操作样例

1. 拖入 **获取邮件(Outlook)** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail20201222.png)

2. 输入 List <MailMessage> 类型的变量到邮件，例：mail，输入邮件文件夹字符串，例如：“收件箱”，输入邮件地址字符串，例：“××@encootech.com”，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122202.png)

1. 拖入 **保存附件** 和 **写入日志** 组件，输入 **保存附件** 的邮件，因为 **获取邮件(Outlook)** 的输出邮件是一个 List，所以这边输入的变量类型是 MailMessage，可以取 maillist 的第一个元素，例：mail[0]，输入文件夹路径，例：“C:\\云扩科技”，输入 **写入日志** 的日志内容，打印出获取的第一个邮件的内容，例：mail[0].Body.ToString()，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122203.png)

4. 点击运行，查看运行结果，检查获取附件和写入日志的邮件内容是否正确：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122204.png)