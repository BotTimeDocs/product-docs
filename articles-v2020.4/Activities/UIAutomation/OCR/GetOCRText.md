# 获取 OCR 文本

## 视频示例

## 概述

对指定元素或图片进行 OCR 并返回结果。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### OCR

- **平台** ：进行 OCR 所使用的平台。
- **AppKey** ：选中平台所需的 AppKey。
- **AppSecret** ：选中平台所需的 AppSecret。

> **说明：**
>
> 当你选择不同的平台进行 OCR 识别时，你需要购买对应的服务，并使用对应的 AK。参考以下文档获取对应的信息：
>
>- 当你选择“百度”时，参考 [Quickstart](https://cloud.baidu.com/doc/OCR/s/dk3iqnq51) ；
>- 当你选择“阿里”时，参考 [创建 AccessKey](https://help.aliyun.com/document_detail/53045.html?spm=a2c4g.11186623.6.581.1fd87d0aEHqZj6&parentId=43579)；
>- 当你选择“腾讯”时，参考 [一分钟接入服务端 API](https://cloud.tencent.com/document/product/866/34681)。

### 目标

- **控件元素** ：接收变量作为目标元素。属性 **控件元素**、**选择器**、**图片** 和 **图片路径** 四者互斥且必填一。
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定 UI 元素。可通过点击 **指定元素** 自动生成。
- **图片** ：对此图片进行 OCR。
- **图片路径** ：对此路径指向的图片进行 OCR。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待，1000ms = 1s。

### 输出

- **纯文本** ：将 OCR 的结果以纯文本的形式存储在此变量
- **Json 文本** ：将 OCR 的结果以 Json 文本的形式存储在此变量。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：使用腾讯服务识别指定 PDF 的区域的文本，并返回识别结果。

![配置获取 OCR 文本组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOCRText1.png)

![OCR 区域](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OCR-sample.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOCRText3.png)
