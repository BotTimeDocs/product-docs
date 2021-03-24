# HTTP请求

此组件可以发送HTTP请求并返回响应的数据，并支持测试配置的HTTP请求是否可用。

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件。
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件。
- **超时(毫秒)** ：指定此组件的执行时间。单位为毫秒（ms）,1000ms = 1s。默认值为30000，即30秒，包含匹配超时（毫秒）。仅支持整型变量和整型。

### 输入

- **URL** ：输入请求的URL；仅支持字符串变量和字符串。
- **请求方法** ：选择请求的方法，支持GET、POST、HEAD、PUT、DELETE、OPTIONS、PATCH。
- **内容类型** ：选择请求的内容类型，例如：application/json。
- **请求头** ：输入请求头，仅支持Dictionary变量。可在“设置请求方式”弹窗中输入请求头信息，若同时在此属性框和弹窗中指定请求头，则使用弹窗中设置的变量。
- **请求正文** ：输入请求的正文；仅支持字符串变量和字符串。
    >**说明：**
    >
    >在组件的可视化界面中，请求正文对应的内容支持文本模式（默认）和代码模式。
    >
    > - 文本模式（默认）：输入纯文本内容。
    > - 代码模式：输入C#代码。
  
- **超时(秒)** ：输入请求超时秒数；仅支持整型变量和整型值。

### 输出

- **响应正文** ：输出此HTTP请求返回的数据；仅支持变量

## 操作样例

1. 示例中使用阿里云**身份证识别**接口，接口说明：[身份证识别](https://market.aliyun.com/products/57124001/cmapi010401.html?spm=5176.12901015.0.i12901015.6416525cpTr5NW&innerSource=search#sku=yuncode440100000)
2. 接口文档如：

    - **请求方式**：POST
    - **返回类型**：JSON
    - **请求参数（Hearders）**：
    ```
   "Content-Type":"application/json; charset=UTF-8"
   "Authorization":"APPCODE 你的appcode"
    ```
    - **请求参数（Body）**：
    ```
    {
	"image":  "图片二进制数据的base64编码/图片url",
	"configure": {"side":"face"}  #身份证正反面类型:face/back
    }
    ```
3. 拖入**HTTP请求**组件，如下图所示：

    - 设置`方法`： POST
    - 设置`URL`：`"http://dm-51.data.aliyun.com/rest/160601/ocr/ocr_idcard.json"`
    - 设置`内容类型`：`application/json`
    - 设置`Hearders`：
    ```
    "Content-Type":"application/json; charset=UTF-8"
    "Authorization(key)","APPCODE APPcode值(value)"
    ```
    - 设置Boby输入框：支持文本模式和C#代码模式，点击icon切换2种输入方式

    文本模式：支持文本在文本框中输入，例如
    ```
    {"configure": {"side": "face"}, "image": "/9j/4AAQSkZJRgABAQAAAQABAAD(内容太多只放入部分)"}
    ```
    或者
    ```
    {'configure': {'side': 'face'}, 'image': '/9j/4AAQSkZJRgABAQAAAQABAAD(内容太多只放入部分)'}
    ```
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/httprequestid.jpg)

    代码模式C#：支持C#代码语法在文本框中输入，例如side是以变量传入进去
    ```
    "{""configure"": {""side"": """ + side + """}, ""image"": ""/9j/4AAQSkZJRgABA(内容太多只放入部分)""}"
    ```
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/httprequestid_csharp.jpg)

4. 点击`测试`，查看测试结果，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/httpresponse.jpg)

**更多HTTP操作链接**：
[HTTP抓包](https://mp.weixin.qq.com/s/Vo7QVfucAyHhEbHJZWeZXw)