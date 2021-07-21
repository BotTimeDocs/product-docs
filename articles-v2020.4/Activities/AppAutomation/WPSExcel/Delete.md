# 删除数据

## 视频示例

## 概述

对指定工作表进行删除操作。可实现删除&quot; 单元格，整行，整列，区域，工作表&quot;

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **移动单元格** ：勾选时，删除数据同时将移动单元格，移动模式以用户选择为准；不勾选时，仅删除文本且不清空格式
- **移动模式** ：当勾选&quot; 移动单元格&quot; 时，下拉此项选择单元格的移动模式。具体效果实现同 Office Excel

### 输入

- **单元格** ：删除操作的目标单元格地址。若只需删除单个单元格内数据，则填充此项。仅支持字符串变量和字符串
- **工作表** ：执行删除操作的目标工作表。仅支持字符串变量和字符串
- **列** ：删除整列数据。若需删除整列数据，则填充此项（例：1，即删除第一列）。仅支持整型变量和整型
- **区域** ：删除操作的目标单元格区域。若需删除区域数据，则填充此项。仅支持字符串变量和字符串
- **删除整表** ：勾选时，删除指定工作表
- **行** ：删除整行数据。若需删除整行数据，则填充此项（例：1，即删除第一行）。仅支持整型变量和整型

>**说明：**
>
>上述&quot; 输入&quot; 六项，除&quot; 工作表&quot; 外，剩余五项必须五选一且互斥

## 使用示例

1. 新建一个 Excel 文件，在 A1: B7 处填入需要被读取的值:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps9.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **删除数据** 组件至 **打开/新建** 组件中，填写工作表和列号:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps27.png)

4. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps28.png)
