# 条件(Switch)

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Switch.mp4"></video>

## 概述

指定 C#表达式，并根据每个 Case 判断执行符合条件的流程。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **表达式** ：输入 C#表达式

switch 语句的一般形式为：

```c#
    switch(表达式){
    case 常量表达式 1:  语句 1;
    case 常量表达式 2:  语句 2;
    … 
    case 常量表达式 n:  语句 n;
    default:  语句 n+1;}

```

 意思为先计算表达式的值，再逐个和 case 后的常量表达式比较，若不等则继续往下比较，若一直不等，则执行 default 后的语句；若等于某一个常量表达式，则从这个表达式后的语句开始执行，并执行后面所有 case 后的语句。

## 使用示例

**此流程执行逻辑**：当满足表达式值时，输出对应的提示信息，当不满足表达式值时，输出另外的对应的提示信息。

![配置条件(Switch)组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-3.png)
