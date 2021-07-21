# 判断OCR文本是否存在

## 视频示例

## 概述

对指定元素或图片进行OCR，并判断指定文本是否存在，将其结果存储在输出属性**OCR元素**内。不支持图像识别指定元素

## 属性

### OCR

- **平台** ：进行OCR所使用的平台
- **AppKey** ：选中平台所需的AppKey。仅支持字符串变量和字符串
- **AppSecret** ：选中平台所需的AppSecret。仅支持字符串变量和字符串

>**说明：**
当你选择不同的平台进行 OCR 识别时，你需要购买对应的服务，并使用对应的 AK。参考以下文档获取对应的信息：
- 当你选择 *百度* 时，参考 [Quickstart](https://cloud.baidu.com/doc/OCR/s/dk3iqnq51) ；
- 当你选择 *阿里* 时，参考 [创建 AccessKey](https://help.aliyun.com/document_detail/53045.html?spm=a2c4g.11186623.6.581.1fd87d0aEHqZj6&parentId=43579)；
- 当你选择 *腾讯* 时，参考 [一分钟接入服务端 API](https://cloud.tencent.com/document/product/866/34681)。

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：接收变量作为目标元素。属性**控件元素**、**选择器**、**图片**和**图片路径**四者互斥且必填一
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定UI元素。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串
- **图片** ：对此图片进行OCR。
- **图片路径** ：对此路径指向的图片进行OCR。
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输入

- **文本** ：判断此文本是否存在并将结果存储在输出属性**结果**内。仅支持字符串变量和字符串
    注意：**文本** 输入框中支持正则表达式。如果你希望使用正则表达式进行匹配，请直接输入正则表达式。
- **出现次数** ：当指定元素中有若干指定文本出现时，此项用于指定获取第几次出现的元素。仅支持整型变量和整型

### 输出

- **结果** ：将判断存储在此变量。仅支持布尔变量

## 使用示例

1. 拖入**判断OCR文本是否存在**组件，指定元素，设置厂家，厂家AppKey和AppSecret（以腾讯OCR为例）等属性：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IdentifyOCRTextExist1.png)

   **OCR 区域**：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OCR-sample.png)

3. 拖入**点击**组件，接收的输入控件元素为前一步返回的对象：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IdentifyOCRTextExist2.png)

3. 运行流程并查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IdentifyOCRTextExist3.png)
