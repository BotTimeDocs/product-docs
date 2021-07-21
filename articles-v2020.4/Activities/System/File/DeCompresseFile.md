# 解压缩文件

## 视频示例

## 概述

对指定的 ZIP 或 RAR 压缩文件进行解压缩。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **密码**：输入压缩密码，可接变量。可与 **设置密码** 组件配合使用。
- **同名替换**：有同名文件是否替换。

### 输入

- **解压至文件夹**：选择或输入需要解压到的文件夹路径，支持相对路径或绝对路径，可接变量。
- **压缩文件路径**：选择需要被解压的压缩文件路径，支持相对路径或绝对路径，可接变量。

## 使用示例

1. 拖入一个 **解压缩文件** 组件至流程中。
2. 双击打开该组件，配置该组件的属性，如下图所示。

    - 压缩文件路径：选择压缩文件所在的路径，如，"C:\Users\wangxin\Desktop\test.rar"。
    - 解压至文件夹：选择或输入需要解压到的文件路径，如，"C:\Users\wangxin\Desktop"。

    ![解压缩文件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decompressefile20210225.png)

3. 保存并运行流程。
4. 在目标路径下，查看运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decompressefileresult20210225.png)