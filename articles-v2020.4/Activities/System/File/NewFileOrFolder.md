# 新建文件/文件夹

## 视频示例

<video controls height='450px' width='800px' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/CreateFileOrFolder.mp4"></video>

## 概述

新建文件或文件夹到指定位置。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **路径** ：新建文件或文件夹的全路径。支持相对和绝对路径。若全路径中包含不存在的文件夹，则自动新建。
- **路径类型** ：下拉框选择新建文件或文件夹。

### 可选项

- **同名替换**：若有同名文件/文件夹则替换。

   - 勾选时：若有同名文件/文件夹则替换。
   - 不勾选时（默认不勾选）：有同名文件/文件夹则报错：“新建失败，有相同名称文件/文件夹”。

## 使用示例

**此流程执行逻辑**：在D盘中新建一个“新建DOC文档.doc”文件。

![配置新建文件/文件夹组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/newFile-2.png)
