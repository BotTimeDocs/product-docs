# 安卓手机获取短信验证码

## 概述

在一些自动化应用场景中，经常需要获取手机的短信验证码，如，登录界面中的验证码。

![获取短信验证码应用场景](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/smscode20210818.png)

云扩RPA目前支持两种方式获取安卓手机的短信验证码，如下文所述。

## 方式一：使用【获取短信验证码】组件

通过使用编辑器中的 **获取短信验证码** 组件并与安卓真机建立连接后，获取手机上的短信验证码，具体参见 [获取短信验证码](./../Activities/PhoneAutomation/MobileGetSmsCode.md) 组件。

## 方式二：安装指定应用

在安卓手机上安装 [EncooSmsObserver.apk](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/EncooSmsObserver.apk) 并独立运行该应用，通过配置指定 API 地址获取手机上的短信验证码。

> **说明：**
>
> 该应用正常情况下，会一直轮询，将符合条件的短信发送至 API 中，每次只能获取一个短信验证码。

![应用界面](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/encoosmsobserver202108181.png)

- **手机号码**：需要获取短信来源的手机号，支持指定手机号或正则表达式。
- **API 地址**：手机在当前规则下获取到的短信信息需发送到的 API 地址（API 服务需自行部署）。

    > **说明：**
    >
    > 手机端将获取到的信息通过 POST 请求，封装在 request body 里发送到 API，API 解析 body，即为短信内容。
