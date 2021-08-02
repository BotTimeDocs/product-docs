# 写入日志

## 视频示例

## 概述

将指定的文本内容打印在流程运行日志中。通常用于在流程日志中增加业务相关信息或关键字段信息，使流程日志更易于阅读和故障排查。

## 属性

### 基本

参见[通用配置项](../Appendix/CommonConfigurationItems.md)。

### 日志

- **日志级别** ：选择Debug后，可查看最详细的日志信息；选择Info后，可查看Info和Error等级的日志信息；选择Error后，将只输出Error日志。
- **日志内容** ：写入日志的内容。

## 使用示例

**此流程执行逻辑**：选择日志级别并填写日志内容后将在“输出面板”中显示日志内容。

   ![写入日志配置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/writelogsetting20201221.png)  

   - 日志级别：下拉选择日志级别，如，Info
   - 日志内容：输入日志内容，如，"这里是写入的日志内容"
  
**执行结果**：

   ![查看运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/writelogoutput20201221.png)