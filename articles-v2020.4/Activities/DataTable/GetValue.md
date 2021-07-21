# 获取单元格的值

## 视频示例

## 概述

将数据表内指定单元格内值的存储到输出值变量。结合**筛选**组件一起使用，当输出的是一个一行一列的数据表时，此组件输入属性坐标为（1，1）时，可实现取数据表中特定坐标值的效果，变相实现查找（例姓名为张三的成绩）

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数据表** ：读取此数据表中的值
- **行索引** ：指定要获取数据表值的行索引。仅支持整型变量和整型
- **列索引** ：指定要获取数据表值的列索引。仅支持整型变量和整型

### 输出

- **值** ：将获取到数据表内的单元格值存储到此变量

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateRow20201228.png)

3. 拖入**获取单元格的值**组件和**写入日志**组件，输入填入数据表变量，例：table，输入单元格行索引和列索引，默认从0开始，例如：1和1（表示的第二行第二列），创建一个Object类型的变量用来接收输出的单元格的值，例：cellvalue，输入日志内容把单元格值打印出来，例："获取的单元格的值是："+cellvalue.ToString()，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetValueDataTable20201229.png)

4. 点击运行，查看运行结果，检查写入日志的单元格值是否为数据表第二行第二列的值17：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetValueDataTable2020122902.png)
