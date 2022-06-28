# 设置日志级别

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/SettingLogLevel.mp4"></video>

## 概述

控制日志输出的内容。此组件后的日志将按照所选级别输出。

> **说明**：
>
> 编辑器默认日志输出级别为 Info，设置此组件“日志级别”属性为 Debug 后，可以查看更加详细的日志信息。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 日志

- **日志级别** ：共有三个选项：Debug,  Info, Error。选择 Debug 后，可查看最详细的日志信息；选择 Info 后，可查看 Info 和 Error 等级的日志信息；选择 Error 后，将只输出 Error 日志。

## 使用示例

**此流程执行逻辑**：设置日志级别为 `Debug`, 运行流程后，“输出面板”中输出 Debug，Info，Error 等级的日志信息。

![配置设置日志级别组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-3.png)
