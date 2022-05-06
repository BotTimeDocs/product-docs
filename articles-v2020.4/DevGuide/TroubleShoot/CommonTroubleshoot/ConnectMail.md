# 邮箱连不上

## 限制条件

- 使用最新版本的编辑器
- 建议不要在虚拟机环境中使用

## 根本原因

常见原因如下：

- 服务器地址和端口的问题

    > 国际版和国内版的服务器地址不一样

- 账号/密码不正确
- 公共邮箱有问题

## 常见排查步骤

1. **【报错信息】：[错误] 连接服务器失败。详细错误信息：由于连接方在一段时间后没有正确答复或连接的主机没有反应，连接尝试失败。**

    解决办法：

    - Step1：查看自己邮箱设置里面的 smtp 配置（参考 163 的配置），通常私有的邮箱服务器会自己配置 smtp, pop3 等服务。

        > 说明：
        >
        > QQ 邮箱配置可参考：(<https://service.exmail.qq.com/cgi-bin/help?subtype=1&id=28&no=1000585>)

    - Step2：参照邮件类组件的使用 [说明文档](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/Mail/SendOutlookMail.md?uuid=e9578822-8a59-4f6d-bf84-c62718f5b6b3) 确认配置的属性是否有误。
