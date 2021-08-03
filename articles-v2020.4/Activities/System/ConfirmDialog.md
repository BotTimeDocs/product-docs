# 确认框

## 视频示例

<video controls height='450px' width='800px' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ConfirmBox.mp4"></video>

## 概述

以弹框形式将需要人工确认的信息展现出来，并可通过用户的确认结果来做后续判断与流程走向的控制。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **标题** ：弹出的确认框的标题。
- **描述** ：弹出的确认框中，需要确认的描述信息。

### 输出

- **确认结果** ：将确认结果的值存储在此变量。点击“确认”按钮后的返回值为True; 点击“取消”按钮后的返回值为False。
  
## 使用示例

**此流程执行逻辑**：通过配置确认框中显示的内容，最终显示真实的确认对话框，供用户确认结果。

![确认框配置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/comfirmsetting20201221.png)  

**运行结果**：

![查看运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/showresult20201221.png)

>**说明：**
>
>选中弹框中显示的内容，鼠标右键，可复制其内容。
