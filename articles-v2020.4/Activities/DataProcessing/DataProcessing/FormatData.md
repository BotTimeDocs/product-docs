# 数据格式化

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/DataFormat.mp4"></video>

## 概述

支持输入 DateTime、Int 等类型数据并转换成符合实际业务需要的数据格式（数值、百分比、货币和日期时间）。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据** ：被格式化的原数据；支持 Int、Int32、Int64、Float、Double、DateTime 等数据类型。

### 输出

- **格式化数据** ：将格式化后返回的值存储在此变量；支持 String 数据类型。

## 使用示例

**此流程执行逻辑**：将数据`1234560.789`以数值类型且保留两位小数输出至变量`变量b`中。

![配置数据格式化组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData2.png)
