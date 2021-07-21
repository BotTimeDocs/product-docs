# 合并单元格

## 视频示例

## 概述

将指定区域内单元格合并，并返回合并后的值

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：合并区域所属工作表。仅支持字符串变量和字符串
- **区域** ：执行合并操作的目标区域。仅支持字符串变量和字符串

### 输出

- **合并值** ：将合并后单元格内显示的值存储在此变量

## 使用示例

1. 拖入 **打开/新建** 组件，勾选是否新建文件，再填入需要打开或者新建的 Excel 文件，并配置所需选项内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps1.png)

2. 双击 **打开/新建** 组件，拖入 **合并单元格** 组件，并设置工作表名称和合并区域:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps60.png)

3. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps61.png)
