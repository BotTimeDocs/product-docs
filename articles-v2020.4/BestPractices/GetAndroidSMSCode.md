# 安卓手机获取短信验证码

## 概述

在一些自动化应用场景中，经常需要获取手机的短信验证码，如，登录界面中的验证码。

![获取短信验证码应用场景](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/smscode20210818.png)

云扩 RPA 目前支持四种方式获取安卓手机的短信验证码，如下文所述。

  - [方式一：通过组件调用](#方式一通过组件调用)
  - [方式二：通过 API 地址](#方式二通过-api-地址)
  - [方式三：通过邮箱地址](#方式三通过邮箱地址)
  - [方式四：通过 WebHook](#方式四通过-webhook)

## 方式一：通过组件调用

通过使用编辑器中的 **获取短信验证码** 组件并与安卓真机建立连接后，获取手机上的短信验证码，具体参见 [获取短信验证码](./../Activities/PhoneAutomation/MobileGetSmsCode.md) 组件。

## 方式二：通过 API 地址

在安卓手机上打开已安装的“云扩手机验证码监听器”应用，通过配置指定 API 地址获取手机上的短信验证码。

> **说明：**
>
> 该应用正常情况下，会一直轮询，将符合条件的短信发送至 API 中，每次只能获取一个短信验证码。

1. **下载 Android 服务端**：在 [云扩 RPA 控制台（企业版）](https://console.encoo.com/) 的 **首页** 中下载最新版本 Android 服务包。

2. **安装“云扩手机验证码监听器”应用**：
  
    a. 将已下载的“Android 服务端”压缩包进行解压缩

    b. 在“Encoo.Android.Automation/apk”路径下，找到“云扩手机验证码监听器”应用

    c. 通过数据线与真机进行连接，点击安装此应用于手机端

    ![手机端验证码应用路径](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/apkpath20210831.png)

3. **配置“云扩手机验证码监听器”应用**：根据如下配置项配置后，单击“开始监听”按钮。

    ![应用界面](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/apipath20210831.jpg)

    - **监听手机号**：需要获取短信来源的手机号，支持指定手机号或正则表达式，如，`183xxxx1256`。
    - **API 地址**：手机在当前规则下获取到的短信信息需发送到的 API 地址（API 服务需自行部署），如，`http://xxxx`。

        > **说明：**
        >
        > 手机端将获取到的信息通过 POST 请求，封装在 request body 里发送到 API，API 解析 body，即为短信内容。

## 方式三：通过邮箱地址

在安卓手机上打开已安装的“云扩手机验证码监听器”应用，通过配置指定邮箱地址获取手机上的短信验证码。

> **说明：**
>
> 该应用正常情况下，会一直轮询，将符合条件的短信发送至指定邮地址中，每次只能获取一个短信验证码。

1. **下载 Android 服务端**：在 [云扩 RPA 控制台（企业版）](https://console.encoo.com/) 的 **首页** 中下载最新版本 Android 服务包。

2. **安装“云扩手机验证码监听器”应用**：
  
    a. 将已下载的“Android 服务端”压缩包进行解压缩

    b. 在“Encoo.Android.Automation/apk”路径下，找到“云扩手机验证码监听器”应用

    c. 通过数据线与真机进行连接，点击安装此应用于手机端

    ![手机端验证码应用路径](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/apkpath20210831.png)

3. **配置“云扩手机验证码监听器”应用**：根据如下配置项配置后，单击“开始监听”按钮。

    - **配置发送邮件的邮箱信息**：单击“云扩手机验证码监听器”应用的右上角的“邮箱配置”，按照提示配置发送邮件的邮箱信息，支持基于 SMTP 的方式。

        ![发件箱配置](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/sendmail20210831.jpg)
  
    - **配置接收邮件的邮箱信息**：

        ![收件箱配置](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/receivemail20210831.jpg)

        - **监听手机号**：需要获取短信来源的手机号，支持指定手机号或正则表达式，如，`183xxxx1256`。

        - **邮箱地址**：手机在当前规则下获取到的短信信息需发送到的邮箱地址，如，`xxx@encootech.com`。

## 方式四：通过 WebHook

通过 WebHook 的方式，支持“**企业微信**”和“**钉钉**”类型，具体使用入口同上述几种方式，具体配置信息如下。

![WebHook](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/wechatwebhook20211214.png)

- **监听手机号**：需要获取短信来源的手机号，支持指定手机号或正则表达式，如，`183xxxx1256`。

- **WebHook 地址**：手机在当前规则下获取到的短信信息需发送到的邮箱地址，如，`https://qyapi.weixin.qq.com/cgi-bin/webhook/send?key=693axxx6-7aoc-4bc4-97a0-0ec2sifa5aaa`。
- **关键词**：content 内容，如，`hello world`。
