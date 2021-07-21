# 添加数据列

## 视频示例

## 概述

向数据表中添加一列，并自动保存同步至指定数据表

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：将数据列添加到此表
- **数据表列** ：添加到数据表的数据表列对象。和&quot;列名&quot;属性两者互斥，只能且必需填入一项
- **列名** ：点击可打开&quot;添加列&quot;的窗口，自定义列信息。和&quot;数据表列&quot;属性两者互斥，只能且必需填入一项

    >**说明：**
    >
    >当“添加列”弹框中勾选“整形自动加一”选项时，不会对已有行数据做更改，只有新加行时，生效。

    ![添加列](https://docimages.blob.core.chinacloudapi.cn/images/Activities/addcolumn20210512.png)

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 拖入**添加数据列**组件和**预览数据表**组件，输入数据表变量，例：table，点击设置输入列名信息,例：“职业”，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddColumn20201228.png)

4. 点击运行，查看运行结果，检查预览出的数据表是否增加了“职业”数据列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddColumn2020122802.png)