# 文档理解

可实现根据在企业版控制台设置的文档理解模板对文件识别。在编辑器或机器人运行时基于当前激活信息的控制台权限。
>**说明**
>
>仅支持企业版（私有化部署），且需购买控制台中的**文档理解服务**后方可使用该功能。


## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件
- **超时（毫秒）**：指定此组件的执行时间。单位为毫秒（ms）,1000ms = 1s。包含匹配超时（毫秒）。若超出此时间，组件还未执行，会抛出错误。


### 输入

- **资源组** ：输入或从下拉列表选择资源组。支持字符串变量或字符串。
- **模板名称** ：输入或从下拉列表选择配置的文档理解模板名称。支持字符串变量或字符串。
- **文件路径** ：输入欲被识别的文件路径，支持PDF或图片格式文件。支持字符串变量或字符串。

### 输出

- **识别结果** ：输出识别的结果（JSON），仅支持字符串变量。

## 操作样例

1. 拖入**文档理解**组件至项目流程中，并设置变量result(String)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DocReader_1.png)

2. 双击打开文档理解，选取PDF，例："D:\\测试.PDF"，输入PDF路径，选择资源组和模板名称，在输出中添加变量result,如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DocReader_2.png)

3. 点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DocReader_3.png)

   >**说明：**
   >
   >组件需要私有化部署，控制端设置如下图所示：

   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DocReader_4.png)
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DocReader_5.png)
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DocReader_6.png)

