# 文档理解

## 视频示例

## 概述

可实现根据在企业版控制台设置的文档理解模板对文件识别。在编辑器或机器人运行时基于当前激活信息的控制台权限。
>**说明**
>
>仅支持企业版（私有化部署），且需购买控制台中的**文档理解服务**后方可使用该功能。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **模板名称** ：输入或从下拉列表选择配置的文档理解模板名称。支持字符串变量或字符串。
- **文件路径** ：输入欲被识别的文件路径，支持PDF或图片格式文件。支持字符串变量或字符串。
- **资源组/部门** ：输入或从下拉列表选择资源组。支持字符串变量或字符串。

### 输出

- **识别结果** ：输出识别的结果（JSON），仅支持字符串变量。

## 使用示例

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

