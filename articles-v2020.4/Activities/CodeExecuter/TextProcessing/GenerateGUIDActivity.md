# 生成GUID

## 视频示例

## 概述

获取一个新的GUID。

>**说明:**
>
>全局唯一标识符（GUID，Globally Unique Identifier）是一种由算法生成的二进制长度为128位的数字标识符。在 Windows 平台上，GUID 广泛应用于微软的产品中，用于标识如注册表项、类及接口标识、数据库、系统目录等对象。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **GUID** ：输出生成的GUID的值存储于该变量中，仅支持字符串变量。
## 使用示例

1. 拖入**生成GUID**组件至项目流程中
![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GenerateGUIDActivity2021010501.png)

2. 拖入其它组件至流程中，例：**写入日志**组件，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GenerateGUIDActivity2021010502.png)

3. 点击运行，成功生成GUID，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GenerateGUIDActivity2021010503.png)