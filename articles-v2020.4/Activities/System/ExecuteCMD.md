# 执行命令行

## 视频示例

## 概述

执行CMD命令行，并提供返回值。例如使用命令行实现60秒后定时关机： &quot;shutdown -s -t 60&quot;
>**说明：**
>
>此组件也支持对Python文件的操作，例如：在“命令行”属性中填写“Python Test.py arg1 arg2”, 其中“arg1”和“arg2”为参数。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作目录** ：指定运行命令的工作目录
- **命令行** ：执行该命令行。仅支持字符串变量和字符串

### 输出

- **输出** ：将命令行执行后的结果存储到此变量

## 使用示例

1. 拖入**执行命令行**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-1.png)

2. 双击进入组件内部，设置参数：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-2.png)

3. 拖入**写入日志**组件，可以输出执行命令行的结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-3.png)

4. 运行流程，查看控制台的输出：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-4.png)
