# 设置/重置密码

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ResetPassword.mp4"></video>

## 概述

对 Excel 文件进行增加、更新或去除密码。

> **说明：**
>
> 该组件需在 Office Excel 的 **打开/新建** 组件内进行使用。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **密码** ：若为空则去除当前 Excel 文件密码；若不为空则对 Excel 文件增加或更新密码。

## 使用示例

**前置必要组件**：[打开/新建](../../TableExcelWPS/OpenExcel.md)

**此流程执行逻辑**：给指定路径下的 Excel 文件设置密码。

![配置重置密码组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ResetPassword1.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ResetPassword2.png)