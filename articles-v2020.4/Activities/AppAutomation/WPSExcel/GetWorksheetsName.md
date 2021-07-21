# 获取所有工作表名

## 视频示例

## 概述

获取工作簿内所有工作表名称。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输出

- **工作表名称** ：工作簿内所有工作表名存储到此变量。可结合循环组件输出或使用工作表名

## 使用示例

1. 拖入 **打开/新建** 组件，勾选是否新建文件，再填入需要打开或者新建的 Excel 文件，并配置所需选项内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps1.png)

2. 双击 **打开/新建** 组件，拖入 **获取所有工作表名** 组件，设置一个变量来接收输出的工作表名称:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps41.png)

3. 拖入 **循环操作** 组件，设置循环体为步骤 2 中获取的工作表名称的变量，然后拖入 **写入日志** 组件到 **循环操作** 组件中，设置打印内容为 item:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps42.png)

4. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps43.png)