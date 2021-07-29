# 解压缩文件

## 视频示例

## 概述

对指定的 ZIP 或 RAR 压缩文件进行解压缩。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **解压至文件夹**：选择或输入需要解压到的文件夹路径，支持相对路径或绝对路径。
- **压缩文件路径**：选择需要被解压的压缩文件路径，支持相对路径或绝对路径。

### 可选项

- **密码**：输入压缩密码，可接变量。可与 **设置密码** 组件配合使用。
- **同名替换**：有同名文件是否替换。

## 使用示例

**此流程执行逻辑**：将桌面上的`test.rar`文件，解压至桌面。

![解压缩文件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decompressefile20210225.png)

**执行结果**：

![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decompressefileresult20210225.png)