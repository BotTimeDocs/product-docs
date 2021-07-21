# 并行

## 视频示例

## 概述

同时执行此组件内所包含的纵向序列

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **结束条件** ：设置结束执行的条件

## 使用示例

1. 拖入**并列**组件并双击展开，拖入两个**序列**组件，并重命名为“序列-左侧”与“序列-右侧”，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pallel-1.png)

2. 双击展开左右两次序列，并拖入一些相关组件，做好备注，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pallel-2.png)

3. 保存并点击运行流程，查看输出日志，了解并行组件功能：左侧流程延迟时间段内会运行右侧流程，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pallel-3.png)
