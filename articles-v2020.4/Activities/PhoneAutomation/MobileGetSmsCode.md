# 获取短信验证码

获取手机的短信验证码信息。

> **说明：**
>
> - 使用此组件之前请确保手机安装了 SmsObserver.apk 应用，并授予相关短信权限，可参见 [安装 App 应用](../../Studio/process/developProject/MobileDevicesManage/AutomationConfiguration.md)。
> - 目前仅支持 Andriod 手机。

## 属性

### 基本

- **后延迟（毫秒）**：在执行组件操作之后的延迟时间（以毫秒为单位）。
- **前延迟（毫秒）**：在开始执行组件操作之前的延迟时间（以毫秒为单位）。

- **失败后继续**：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。

- **显示名称**：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。

### 可选项

- **来源号码**：验证码短信的来源号码。
- **正则匹配**：用来进行短信验证码内容匹配，支持正则表达式。

    > **说明：**
    >
    > 此处填写的正则表达式，仅对获取到的验证码（如，548721）再进行正则过滤匹配。

### 输入

- **开始时间**：输入日期类型的变量，用来过滤该时间点以后的短信内容。
- **超时（秒）**：在该时间内进行轮询，如果匹配到结果将返回验证码信息，而匹配超时将导致该组件执行失败，默认为超时 60 秒。

### 输出

- **验证码**：获取到的验证码内容。

## 操作样例

1. 拖入一个连接设备组件至流程中，具体参见 [连接设备组件 - 操作样例](./MobileConnect.md)。

2. 在连接设备组件内按照顺序搭建流程，如下图所示。

    ![流程图](https://docimages.blob.core.chinacloudapi.cn/images/Activities/workflowsmscode20201230.jpg)

3. 配置流程中各组件，说明如下：

    - **打开应用软件**：单击指定元素，选择需要打开的手机应用，如，爱康约体检查报告
    - **赋值**：定义一个 DateTime 类型的变量，并获取当前时间，如，Starttime = System.DateTime.Now
    - **点击**：指定元素为手机上应用中的发送验证码按钮。
    - **获取短信验证码**：配置获取短信验证码的输入和输出属性，如下图所示。

     ![配置获取短信验证码](https://docimages.blob.core.chinacloudapi.cn/images/Activities/smscodevarials20201230.png)

    - **写入日志**：输出验证码信息。

4. 保存并运行流程。

5. 运行过程中，在手机端可看到效果如下：

    ![手机端效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/runprocesssmscode20201230.png)

6. 在输出框中也可查看运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/resultsmscode20201230.png)

## 常见问题

1. Q：为何获取不到短信验证码？
   <br> A：检查手机短信验证码安全保护是否禁止，若开关打开，则无法获取到验证码。

   > **说明：**
   >
   > 不同品牌不同型号的手机，设置路径有所不同。

   - 华为手机，在“信息”的右上角的“设置”中设置“验证码安全保护”为“不勾选”状态。

    ![华为手机短信安全设置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/smssetting20201230.png)

   - OPPO 手机，在“设置 > 信息”中设置“验证码安全保护”为“不勾选”状态。

    ![OPPO 手机短信安全设置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/opposetting20210618.png)
