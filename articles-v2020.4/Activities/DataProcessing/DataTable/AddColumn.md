# 添加数据列

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/AddDataColumn.mp4"></video>

## 概述

向数据表中添加一列，并自动保存同步至指定数据表。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将数据列添加到此表
- **数据表列** ：添加到数据表的数据表列对象。和“列名”属性两者互斥，只能且必需填入一项。
- **列名** ：点击可打开“添加列”的窗口，自定义列信息。和“数据表列”属性两者互斥，只能且必需填入一项。

    >**说明：**
    >
    >当“添加列”弹框中勾选“整形自动加一”选项时，不会对已有行数据做更改，只有新加行时，生效。

    ![添加列](https://docimages.blob.core.chinacloudapi.cn/images/Activities/addcolumn20210512.png)

## 使用示例

**前置必要组件**：[搭建数据表](../DataTable/BuildDataTable.md)

**此流程执行逻辑**：将已搭建的数据表，增加“职业”列。

![配置添加数据列组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddColumn20201228.png)
