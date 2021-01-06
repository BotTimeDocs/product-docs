# HTTP请求

此组件可以发送HTTP请求并返回响应的数据，并支持测试配置的HTTP请求是否可用

## 属性

### 基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件
- **超时(毫秒)** ：指定此组件的执行时间。单位为毫秒（ms）,1000ms = 1s。默认值为30000，即30秒，包含匹配超时（毫秒）。仅支持整型变量和整型

### 输入

- **URL** ：输入请求的URL；仅支持字符串变量和字符串
- **请求方法** ：选择请求的方法，支持GET、POST、HEAD、PUT、DELETE、OPTIONS、PATCH
- **内容类型** ：选择请求的内容类型，例如：application/json
- **请求头** ：输入请求头，仅支持Dictionary变量。可在“设置请求方式”弹窗中输入请求头信息，若同时在此属性框和弹窗中指定请求头，则使用弹窗中设置的变量
- **请求正文** ：输入请求的正文；仅支持字符串变量和字符串
- **超时(秒)** ：输入请求超时秒数；仅支持整型变量和整型值

### 输出

- **响应正文** ：输出此HTTP请求返回的数据；仅支持变量

## 操作样例
1. 示例中使用阿里云**汇率转换**接口，链接如下：
https://market.aliyun.com/products/57000002/cmapi011221.html?spm=5176.12901015.0.i12901015.17e2525cz4KoQ4&innerSource=search_%E6%B1%87%E7%8E%87%E6%9F%A5%E8%AF%A2%E8%BD%AC%E6%8D%A2#sku=yuncode522100006
2. 接口文档，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPRequest1.png)
3. 拖入**HTTP请求**组件，如下图所示：
- 设置`方法`： GET
- 设置`URL`：
`https://jisuhuilv.market.alicloudapi.com/exchange/convert?amount=10&from=CNY&to=USD`
- 设置`内容类型`：`none`
- 设置`头部`：`Authorization(key)`,`APPCODE APPcode值(value)`：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPRequest2.png)

4. 点击`测试`，查看测试结果，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPRequest3.png)
