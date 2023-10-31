# 上传文件

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/UploadFile.mp4"></video>

## 概述

将本地文件上传至云扩 RPA 控制台（企业版）的“数据中心 > 文件服务”中。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **本地文件路径**：选择待上传的文件路径。
- **部门**：填写控制台中文件/文件夹所在的部门。
- **目标位置**：选择控制台文件服务中的文件夹路径作为待上传文件的路径 。

### 输出

- **结果**：将返回的结果存储至此变量。

### 可选项

- **同名替换**：是否在同一目录下有相同名称的文件时替换原文件。
    - 勾选后：在同一目录下有相同文件时，则替换原文件。
    - 不勾选：在同一目录下有相同文件时，则弹框提示“已有同名文件存在”。

## 使用示例

**此流程执行逻辑**：将本地文件"执行CSharp代码.xaml"上传至控制台文件服务中的文件夹"Test_demo"路径下。

![配置属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/uploadfile20210105.png)
