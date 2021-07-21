# 读取CSV文件

## 视频示例

## 概述

将一个CSV文件读取，存储到数据表变量

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **编码方式** ：文件的编码方式。可以在 [此处](../Appendix/Encoding.md) 找到每个字符编码的完整代码列表。要指定要使用的编码类型，请使用&quot; 名称&quot;字段中的值。如果未指定编码类型，则活动将搜索文件的字节顺序标记以检测编码。如果未检测到字节顺序标记，则默认选择UTF-8。仅支持字符串变量和字符串
- **分隔符** ：指定CSV文件的分隔符。此属性可不填写，默认使用逗号。仅支持字符变量和字符
- **列名重复加一**：勾选后，若出现重复列名则在原列名后加下划线和数字（默认是1，如果依然重复则+2，依次类推），如：原列名_N

### 输入

- **文件路径** ：要读取的CSV文件路径。支持相对和绝对路径。可在组件面板点击弹出对话框，选择目标文件；亦支持手动输入路径，若路径不存在，则运行失败会报错。仅支持字符串变量和字符串

### 输出

- **数据表** ：将输入的CSV文件存储到此变量，并可取此变量进行数据表相关组件进行操作

## 使用示例

1. 拖入**读取CSV文件**组件，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，创建类型为String的路径变量并给出默认值，例：filepath:"C:\云扩科技\savetable.csv"，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCSV20201229.png)

3. 拖入**预览数据表**组件，输入数据表变量，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCSV2020122902.png)

4. 点击运行，查看运行结果，检查预览出的数据表是否与CSV文件中一致：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCSV2020122903.png)