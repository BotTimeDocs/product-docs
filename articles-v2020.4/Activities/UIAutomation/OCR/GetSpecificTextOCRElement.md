# 获取含OCR文本的元素

对指定元素或图片进行OCR，并查找包含指定文本的元素，将其存储在输出属性**OCR元素**内。不支持图像识别指定元素

## 属性

### OCR

- **平台** ：进行OCR所使用的平台
- **AppKey** ：选中平台所需的AppKey。仅支持字符串变量和字符串
- **AppSecret** ：选中平台所需的AppSecret。仅支持字符串变量和字符串
- **匹配条件** ：判断是否包含指定文本时使用的判断规则，完全匹配或者包含

>**说明：**
当你选择不同的平台进行 OCR 识别时，你需要购买对应的服务，并使用对应的 AK。参考以下文档获取对应的信息：
- 当你选择 *百度* 时，参考 [Quickstart](https://cloud.baidu.com/doc/OCR/s/dk3iqnq51) ；
- 当你选择 *阿里* 时，参考 [创建 AccessKey](https://help.aliyun.com/document_detail/53045.html?spm=a2c4g.11186623.6.581.1fd87d0aEHqZj6&parentId=43579)；
- 当你选择 *腾讯* 时，参考 [一分钟接入服务端 API](https://cloud.tencent.com/document/product/866/34681)。
### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件
- **超时(毫秒)** ：指定此组件的执行时间。单位为毫秒（ms）,1000ms = 1s。包含匹配超时（毫秒）。若超出此属性值还未出现，会抛出错误。仅支持整型变量和整型

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：接收变量作为目标元素。属性**控件元素**和**选择器**两者互斥且必填一
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：要获取的特定UI元素。可通过点击**指定元素**自动生成。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输入

- **文本** ：将含有此文本的元素存储在输出属性**OCR元素**内。仅支持字符串变量和字符串。
    注意：**文本** 输入框中支持正则表达式。如果你希望使用正则表达式进行匹配，请直接输入正则表达式。
- **出现次数** ：当指定元素中有若干指定文本出现时，此项用于指定获取第几次出现的元素。仅支持整型变量和整型

### 输出

- **OCR元素** ：将匹配的元素存储在此变量。仅支持字符串变量和字符串

## 使用示例

1. 拖入**获取含OCR文本的元素**组件，指定元素，设置厂家，厂家AppKey和AppSecret（以腾讯OCR为例）等属性：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetSpecificTextOCRElement1.png)

   **OCR 区域**：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OCR-sample.png)

2. 验证元素存在性：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetSpecificTextOCRElement2.png)

3. 拖入**点击**组件，接收的输入控件元素为前一步返回的对象：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetSpecificTextOCRElement3.png)

3. 运行流程并查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetSpecificTextOCRElement4.png)