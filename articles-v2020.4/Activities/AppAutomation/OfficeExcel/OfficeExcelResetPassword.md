# 重置密码

## 视频示例

## 概述

对 Excel 文件进行增加、更新或去除密码。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **密码** ：若为空则去除当前 Excel 文件密码；若不为空则对 Excel 文件增加或更新密码。仅支持字符串变量和字符串

## 使用示例

1. 新建一个 Excel 文件，不设置密码。

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **重置密码** 到 **打开/新建** 组件中，填写密码“123456”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ResetPassword1.png)

5. 运行成功后，打开 excel，需要输入密码。输入 123456 后，正常打开：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ResetPassword2.png)