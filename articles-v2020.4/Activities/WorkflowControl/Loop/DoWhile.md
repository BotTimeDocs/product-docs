# 循环操作（Do While）

## 视频示例

<video controls height='450px' width='800px' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/DoWhile.mp4"></video>

## 概述

先执行后判断。当满足指定条件时，执行后续组件且至少执行一次；结束时再次判断指定条件，当不再满足时，退出循环

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **循环条件** ：执行此循环需满足的条件

## 使用示例

**此流程执行逻辑**：为循环操作（Do While）组件创建变量count，设置数据类型为Int32，默认值为1，并添加循环条件 count <= 3；在循环操作（Do While）容器内拖入**赋值**组件并设置count递增，随着每次的循环对变量赋值。

![设置Do While循环操作组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dowhile-2.png)
