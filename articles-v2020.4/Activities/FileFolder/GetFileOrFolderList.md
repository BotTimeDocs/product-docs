# 获取文件/文件夹列表

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/GetFileOrFolderList.mp4"></video>

## 概述

获取指定路径下的文件或文件夹列表。同时提供选择“遍历子文件夹”选项和通配符筛选列表内容功能。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **遍历子文件夹** ：勾选时，将同时获取指定路径子文件夹内的列表；不勾选时；则只获取指定路径内列表。
- **列表模式** ：下拉框选择文件或文件夹。
- **列表筛选** ：适用此筛选条件返回列表，支持通配符&quot;\*&quot; &quot;?&quot;。
- **路径** ：获取该路径下的文件或文件夹列表。支持相对和绝对路径。可在组件面板点击弹出对话框，选择要获取列表的路径；亦支持手动输入路径，若路径不存在，则运行失败。如果需要获取当前项目路径下的列表，则只输入双引号即可。

### 输出

- **列表** ：将结果列表存储在此变量，返回类型为全路径。

## 使用示例

**此流程执行逻辑**：获取D盘中Shirley文件夹中的文件列表。

![配置获取文件/文件夹列表组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/fileList-2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/fileList-5.png)
