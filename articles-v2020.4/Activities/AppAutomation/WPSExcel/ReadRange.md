# 读取区域

## 视频示例

## 概述

获取工作簿内单元格区域数据并存储在数据表变量内。若单元格区域未指定，则默认读取整表。（可通过变量连接输入实现读取&quot; 行，列，区域，工作表&quot; 功能）

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **列名重复加一**：勾选后，若出现重复列名则在原列名后加下划线和数字（默认是1，如果依然重复则+2，依次类推），如：原列名_N
- **添加列头**：勾选时，将工作表第一行作为新生成数据表的列头；不勾选时，新生成数据表的列头默认为&quot; 1，2，3…&quot;
- **添加筛选**：勾选时，将不读取指定区域内超出过滤范围的数据；不勾选时，将同时读取指定区域内所有数据，包括超出过滤范围的数据

### 输入

- **工作表**：目标单元格区域所在工作表。仅支持字符串变量和字符串
- **区域**：目标单元格区域。若单元格区域未指定，则默认读取整表数据。仅支持字符串变量和字符串

### 输出

- **数据表**：将读取到的目标区域内数据存储在此变量内。仅支持数据表变量

## 使用示例

1. 新建一个 Excel 文件，在 A1: B7 处填入需要被读取的值:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps9.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **读取区域** 组件至 **打开/新建** 组件中，填写工作表和区域范围，在输出数据中写入变量来接收读取的内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps10.png)

4. 拖入 **预览数据表** 组件，来预览读取区域的数据表内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps11.png)

5. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps12.png)
