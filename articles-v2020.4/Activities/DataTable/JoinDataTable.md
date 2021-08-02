# 联结数据表

## 视频示例

## 概述

根据联结条件，将两个数据表联结到一起，并将结果存储到输出输出数据表变量。提供四种联结条件：全连接，内连接，左连接，右连接

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **联结配置** ：点击右侧的按钮，将弹出联结配置窗口。在此窗口可以进行联结条件的设置

### 输出

- **数据表** ：将联结两表后的结果保存到此变量

## 使用示例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 再拖入一次**搭建数据表**组件按步骤2创建数据表table2，搭建的时候可以列名设置一列与表1一样的方便下面的联结操作，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/JoinDataTable20201225.png)

4. 拖入**联结数据表**组件和**预览数据表**组件，双击打开联结数据表，设置联结配置，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/JoinDataTable2020122502.png)

5. 点击运行，查看运行结果，检查预览出的数据表是否是两个表左连接的正确结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/JoinDataTable2020122503.png)
