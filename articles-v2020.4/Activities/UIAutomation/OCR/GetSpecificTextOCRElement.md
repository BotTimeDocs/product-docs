# 获取含 OCR 文本的元素

## 视频示例

## 概述

对指定元素或图片进行 OCR，并查找包含指定文本的元素，将其存储在输出属性 **OCR 元素** 内。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### OCR

- **平台** ：进行 OCR 所使用的平台
- **AppKey** ：选中平台所需的 AppKey。
- **AppSecret** ：选中平台所需的 AppSecret。
- **匹配条件** ：判断是否包含指定文本时使用的判断规则，完全匹配或者包含。

> **说明：**
>
>当你选择不同的平台进行 OCR 识别时，你需要购买对应的服务，并使用对应的 AK。参考以下文档获取对应的信息：
>
>- 当你选择“百度”时，参考 [Quickstart](https://cloud.baidu.com/doc/OCR/s/dk3iqnq51)
>- 当你选择“阿里”时，参考 [创建 AccessKey](https://help.aliyun.com/document_detail/53045.html?spm=a2c4g.11186623.6.581.1fd87d0aEHqZj6&parentId=43579)；
>- 当你选择“腾讯”时，参考 [一分钟接入服务端 API](https://cloud.tencent.com/document/product/866/34681)。

### 目标

- **控件元素** ：接收变量作为目标元素。属性 **控件元素** 和 **选择器** 两者互斥且必填一。
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定 UI 元素。可通过点击 **指定元素** 自动生成。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待，1000ms = 1s。

### 输入

- **文本** ：将含有此文本的元素存储在输出属性 **OCR 元素** 内。

    >**说明：**
    >
    >**文本** 输入框中支持正则表达式。如果你希望使用正则表达式进行匹配，请直接输入正则表达式。

- **出现次数** ：当指定元素中有若干指定文本出现时，此项用于指定获取第几次出现的元素。

### 输出

- **OCR 元素** ：将匹配的元素存储在此变量。仅支持字符串变量和字符串

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

## 使用示例

**此流程执行逻辑**：使用腾讯服务识别指定 PDF 的区域的文本的元素，并返回识别结果。

![配置获取含 OCR 文本的元素组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetSpecificTextOCRElement1.png)

![OCR 区域](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OCR-sample.png)
