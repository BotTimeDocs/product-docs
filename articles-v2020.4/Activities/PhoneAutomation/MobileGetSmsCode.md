# 获取短信验证码

## 视频示例

## 概述

获取手机的短信验证码信息。

> **说明：**
>
> - 使用此组件之前请确保手机安装了 SmsObserver.apk 应用，并授予相关短信权限，可参见 [安装 App 应用](../../Studio/process/developProject/MobileDevicesManage/AutomationConfiguration.md)。
> - 目前仅支持 Andriod 手机。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **开始时间**：输入日期类型的变量，用来过滤该时间点以后的短信内容。
- **超时（秒）**：在该时间内进行轮询，如果匹配到结果将返回验证码信息，而匹配超时将导致该组件执行失败，默认为超时 60 秒。

### 输出

- **验证码**：获取到的验证码内容。

### 可选项

- **来源号码**：验证码短信的来源号码。
- **正则匹配**：用来进行短信验证码内容匹配，支持正则表达式。

    >**说明：**
    >
    >此处填写的正则表达式，仅对获取到的验证码（如，548721）再进行正则过滤匹配。

## 使用示例

**前置必要组件**：[连接设备](./MobileConnect.md)
**此流程执行逻辑**：接收到手机中发送的手机验证码信息。

![配置获取短信验证码](https://docimages.blob.core.chinacloudapi.cn/images/Activities/smscodevarials20201230.png)

**执行结果**：

![手机端效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/runprocesssmscode20201230.png)

## 常见问题

1. Q：为何获取不到短信验证码？
   </br> A：检查手机短信验证码安全保护是否禁止，若开关打开，则无法获取到验证码。

   > **说明：**
   >
   > 不同品牌不同型号的手机，设置路径有所不同。

   - 华为手机，在“信息”的右上角的“设置”中设置“验证码安全保护”为“不勾选”状态。

    ![华为手机短信安全设置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/smssetting20201230.png)

   - OPPO 手机，在“设置 > 信息”中设置“验证码安全保护”为“不勾选”状态。

    ![OPPO 手机短信安全设置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/opposetting20210618.png)
