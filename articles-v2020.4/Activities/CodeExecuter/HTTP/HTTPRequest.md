# HTTP(S)请求

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/HTTPRequest.mp4"></video>

## 概述

此组件可以发送 HTTP(S)请求并返回响应的数据，并支持测试配置的 HTTP(S)请求是否可用。

> **说明：**
>
> 仅支持简单的 HTTPS 请求，暂不支持需要传递证书才能使用的 HTTPS 请求。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **URL** ：输入请求的 URL。
- **超时(秒)** ：输入请求超时秒数。
- **内容类型** ：选择请求的内容类型，例如：application/json。
- **请求方法** ：选择请求的方法，支持 GET、POST、HEAD、PUT、DELETE、OPTIONS、PATCH。
- **请求头** ：输入请求头，仅支持 Dictionary 变量。可在“设置请求方式”弹窗中输入请求头信息，若同时在此属性框和弹窗中指定请求头，则使用弹窗中设置的变量。
- **请求正文** ：输入请求的正文。

    > **说明：**
    >
    > 在组件的可视化界面中，请求正文对应的内容支持文本模式（默认）和代码模式。
    >
    > - 文本模式（默认）：输入纯文本内容。
    > 
    > ![纯文本](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/https001.png)
    > - 代码模式：支持输入C#代码（双引号需要转义），或是直接使用变量。
    > 
    > ![变量](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/https002.png)
  
### 输出

- **响应正文** ：输出此 HTTP 请求返回的数据。

## 使用示例

**此流程执行逻辑**：使用阿里云 **身份证识别** 接口，接口说明：[身份证识别](https://market.aliyun.com/products/57124001/cmapi010401.html?spm=5176.12901015.0.i12901015.6416525cpTr5NW&innerSource=search#sku=yuncode440100000)验证HTTP请求结果。

![配置HTTP(S)请求组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/httprequestid.jpg)

**更多 HTTP 操作链接**：
[HTTP 抓包](https://mp.weixin.qq.com/s/Vo7QVfucAyHhEbHJZWeZXw)

## 常见问题

1. **Q：现需将抓取的数据通过HTTP协议Post请求发送给其它系统，编辑器中哪个组件可以实现？**

    **A：**“HTTP(S)请求”、 “执行C#代码”、“执行Python代码”等组件均可实现。
