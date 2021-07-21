# 获取OCR文本

## 视频示例

## 概述

对指定元素或图片进行OCR并返回结果。不支持图像识别指定元素

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

### 输出

- **纯文本** ：将OCR的结果以纯文本的形式存储在此变量。仅支持字符串变量和字符串
- **Json文本** ：将OCR的结果以Json文本的形式存储在此变量。仅支持字符串变量和字符串

## 使用示例

1. 拖入**获取OCR文本**组件，指定元素，设置厂家，厂家AppKey和AppSecret（以腾讯OCR为例）：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOCRText1.png)

   **OCR 区域**：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OCR-sample.png)

2. 验证元素存在性：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOCRText2.png)

3. 运行流程并查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOCRText3.png)