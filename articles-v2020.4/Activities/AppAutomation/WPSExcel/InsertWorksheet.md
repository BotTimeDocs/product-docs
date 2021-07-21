# 插入工作表

## 视频示例

## 概述

插入新的工作表到工作簿中，可实现新建工作表插入到指定位置，和复制已有工作表插入到指定位置

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **插入位置** ：将新工作表插入到的目标位置。例如&quot; 1&quot;，即插入工作表的位置为第一个。当为空时，默认插入到最后。仅支持整型变量和整型
- **模式** ：插入工作表时的模式选择。含两项：新建工作表，复制工作表
- **新工作表名称** ：插入的新工作表名称。仅支持字符串变量和字符串
- **源工作表名** ：若模式选择&quot; 复制工作表&quot;，此项为必填项，将取此工作表并复制到新工作表。仅支持字符串变量和字符串

## 使用示例

1. 拖入 **打开/新建** 组件，勾选是否新建文件，再填入需要打开或者新建的 Excel 文件，并配置所需选项内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps1.png)

2. 双击 **打开/新建** 组件，拖入 **插入工作表** 组件，并设置插入位置和新工作表名称:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps53.png)

3. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps54.png)
