# 遍历文件夹

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/TraverseFolders.mp4"></video>

## 概述

遍历指定的文件夹并获取文件路径（默认为变量filePath），可在此组件范围内根据实际业务需要拖入其他组件。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **文件夹** ：输入欲遍历的文件夹路径，支持绝对和相对路径。可接变量。

### 可选项

- **文件筛选** ：输入欲筛选的文件类型，默认为空即获取所有文件；支持通配符（* 和 ?）或指定文件名称，例如：*.xls 或 ?.jpg
- **遍历子文件夹** ：默认为False，即不遍历子文件夹。勾选后则遍历指定“文件夹”下的子文件夹

## 使用示例

**此流程执行逻辑**：查看指定文件夹路径下的文件路径，并输出至“输出面板”中。

![配置遍历文件夹组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/foreachFolder-1.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/foreachFolder-3.png)

## 常见问题

1. **Q：需要上传到FTP内一个多级文件夹，但无法在FTP内解压缩多级文件夹，如何上传FTP内一个文件夹？**

    **A：** 目前FTP组件尚不支持上传文件夹，建议使用“系统 > 文件 > 遍历文件夹”组件，结合“组件市场 > FTP工具 > FTP上传"组件，实现流程。

2. **Q: 在组件市场中，使用“FTP工具 > FTP上传”，如何用编辑器上传到FTP内的指定文件夹中，而不是FTP根目录？**

   **A：** 先通过“FTP工具 > FTP连接”组件中配置“FTP文件夹路径”，再通过组合“FTP工具 > FTP获取文件/文件夹列表”遍历上传。

   ![FTP连接](https://docimages.blob.core.chinacloudapi.cn/images/Studio/ftpconnect20210824.jpg)