
## 如何获取邮件并下载附件

## 开始
1. 创建一个项目
2. 在【组件】面板搜索【邮件】或直接在【软件自动化】-【邮件】目录下找到【[获取邮件POP3](https://academy.bottime.com/zh-cn/wiki/Activities/AppAutomation/Mail/GetMailPOP3.md?_v=v2020.1)】组件，并将其拖入进项目中

3. 在项目中点击【获取邮件POP3】组件并在右侧【属性】面板配置所需字段：
    > **服务器**

    > **服务器地址：** 输入服务器地址，例如："smtp.outlook.cn"

    > **端口号：** 输入服务器端口号，若使用公司邮箱，可向公司IT管理员获取

    > **代理：** 非必填项，根据实际业务需要选择是否填写，本节课程中此字段为空

    > **邮件**

    > **邮件地址：** .............

    > **邮件内容格式：** ............
    
    > **密码：** ............

    > **获取封数：** ............


    > **输出**

    > **输出：** ........

4. 在【组件】面板搜索【附件】或直接在【软件自动化】-【邮件】目录下找到【[保存附件](https://academy.bottime.com/zh-cn/wiki/Activities/AppAutomation/Mail/SaveAttachment.md?_v=v2020.1)】组件，并将其拖入进项目中放在【获取邮件】组件后

5. 点击【保存附件】组件并在右侧【属性】面板配置所需字段：
    > **邮件**

    > **文件夹路径：** .............

    > **邮件：** ............


6. 点击【运行】即可完成邮件发送，此时你就可以在【发件人】邮箱中的【已发送】目录和【收件人】邮箱中的【收件箱】看到此邮件了


## 小结
一个简单的发送邮件自动化流程就完成啦, 快去尝试下编写一个邮件自动化流程吧。
后续课程中还为为您讲解[如何获取邮件和下载附件](https://academy.encoo.com/wiki/Studio/ImportNamespaces.md?)

在[这里](https://academy.encoo.com/wiki/Studio/ImportNamespaces.md?)下载本课程示例, 在编辑器工具栏点击【导入项目】选中此示例文件即可完成加载。


## 相关链接
[发送邮件SMTP](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/Mail/SendMailSMTP.md)

[获取邮件POP3](https://academy.bottime.com/zh-cn/wiki/Activities/AppAutomation/Mail/GetMailPOP3.md?_v=v2020.1)

[保存附件](https://academy.bottime.com/zh-cn/wiki/Activities/AppAutomation/Mail/SaveAttachment.md?_v=v2020.1)