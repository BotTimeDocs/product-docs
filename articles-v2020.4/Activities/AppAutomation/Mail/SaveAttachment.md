# 保存附件

## 视频示例

## 概述

将邮件中的附件保存到指定位置。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 邮件

- **邮件** ：取此邮件变量中的附件，执行保存操作。
- **文件夹路径** ：附件保存位置。若出现同名文件则会报错；支持相对和绝对路径；路径不存在则自动新建。

## 使用示例

**此流程执行逻辑**：将获取到的收件箱中的第 1 封邮件中的附件，保存至本地计算机指定路径中。

![配置保存附件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122203.png)
