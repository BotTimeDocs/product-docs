# 删除数据

## 视频示例

## 概述

对指定工作表进行删除操作。可实现删除&quot; 单元格，整行，整列，区域，工作表&quot;

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **移动单元格** ：勾选时，删除数据同时将移动单元格，移动模式以&quot; 用户选择为准；不勾选时，仅删除文本且不清空格式
- **移动模式** ：当勾选&quot; 移动单元格&quot; 时，下拉此项选择单元格的移动模式。具体效果实现同 Office Excel

### 输入

- **单元格** ：删除操作的目标单元格地址。若只需删除单个单元格内数据，则填充此项。仅支持字符串变量和字符串
- **工作表** ：执行删除操作的目标工作表。仅支持字符串变量和字符串
- **列** ：删除整列数据。若需删除整列数据，则填充此项（例：1，即删除第一列）。仅支持整型变量和整型
- **区域** ：删除操作的目标单元格区域。若需删除区域数据，则填充此项。仅支持字符串变量和字符串
- **删除整表** ：勾选时，删除指定工作表

    > **注意：**
    >
    > 上述&quot; 输入&quot; 六项，除&quot; 工作表&quot; 外，剩余五项必须五选一且互斥。

- **行** ：删除整行数据。若需删除整行数据，则填充此项（例：1，即删除第一行）。仅支持整型变量和整型

## 使用示例

1. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖拽 **删除数据** 到 **打开/新建** 组件中，填写 sheet 名称，填写单元格名称，如果不勾选可选项直接删除单元格；如果勾选可选项，勾选移动单元格，选择移动模式整行，运行成功后会删除 "A1" 所在的行。区域的操作同单元格。输入项除“工作表”外其余五项只能选一个，且正确填写：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Delete1.png)

4. 填写 sheet 名称，填写行号，如果不勾选可选项直接删除行；如果勾选可选项，勾选移动单元格，运行成功删除行后下面的行整体上移；列的操作同行：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Delete2.png)

5. 填写 sheet 名称，勾选删除整表，运行成功后删除整个 sheet：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Delete3.png)
