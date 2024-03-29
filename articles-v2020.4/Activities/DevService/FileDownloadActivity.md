# 下载文件

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/DownloadFile.mp4"></video>

## 概述

下载云扩 RPA 控制台“数据中心 > 文件服务”中已上传的文件。

>**说明：**
>
>- 该组件仅在**企业版**中支持。
>- 目前仅支持单个文件下载。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **部门**：填写控制台中文件/文件夹所在的部门。
- **文件路径**：输入或选择控制台文件服务中的文件路径。

### 输出

- **本地文件路径**：输出下载到本地后的绝对路径。

### 可选项

- **保存至目录**：下载的文件被保存至目录路径。
  
  >**说明：**
  >
  >- 若指定目录不存在,则按指定目录进行新建。
  >- 若此项不填写，默认为 windows 的下载目录。

- **超时**：超时时间（时分秒），默认不限制超时时间：00:00:00。

- **同名替换**：被下载的文件保存到文件夹时，若有同名文件时是否替换覆盖原有文件。勾选表示替换，否则为不替换，不替换时在原文件名中增加当前时间的时间戳，如，原文件名-YYYYMMDDhhmmss。

## 使用示例

**前置必要条件**：在控制台“文件服务”中已上传指定的文件。

**此流程执行逻辑**：将控制台中文件服务中上传的文件`"Testdemo/FunctionList_1.Jpeg"`下载至本地指定的文件路径`桌面`中。

![配置下载文件组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/savepath20201216.png)
