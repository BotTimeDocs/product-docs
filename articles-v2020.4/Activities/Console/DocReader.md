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

- **模板名称** ：输入或从下拉列表选择配置的文档理解模板名称。
- **文件路径** ：输入欲被识别的文件路径，支持PDF或图片格式文件。
- **资源组/部门** ：输入或从下拉列表选择资源组。

### 输出

- **识别结果**：输出识别的结果（JSON）。

## 使用示例

**前置必要条件**：在控制台中的“文档理解”服务中已创建文档理解的模板。

![前置必要条件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DocReader_6.png)

**此流程执行逻辑**：将"D:\\测试.PDF"按照控制台中已设定的指定的模板识别，结果保存至`result`变量中。

![配置文档理解模板](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DocReader_2.png)
