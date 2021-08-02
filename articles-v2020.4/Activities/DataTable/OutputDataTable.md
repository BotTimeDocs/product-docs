# 输出数据表

## 视频示例

## 概述

将一个数据表按照选择的格式输出为字符串

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **输出格式** ：按照选择的格式将数据表输出为字符串。包含两个值：CSV,JSON

### 输入

- **数据表** ：要输出的数据表名，取此值代表的数据表并输出为字符串

### 输出

- **输出** ：将输出后的数据表存储到此变量。仅支持字符串变量和字符串

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 拖入**输出数据表**组件并填入上面已经搭建好的数据表变量table，创建String类型的变量来存储输出字符，例：csvstring，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OutputDataTable20201224.png)

4. 拖入**写入日志**组件并填入**输出数据表**组件的输出变量csvstring：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OutputDataTable2020122402.png)

5. 点击运行，查看运行结果，检查输出的数据表与搭建的数据表是否一致：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OutputDataTable2020122403.png)