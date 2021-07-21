# 条件(Switch)

## 视频示例

## 概述

指定 C#表达式，并根据每个 Case 判断执行符合条件的流程

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **表达式** ：输入 C#表达式

    > **说明：**
    > switch 语句的一般形式为：
    >
    > switch(表达式){
    case 常量表达式 1:  语句 1;
    case 常量表达式 2:  语句 2;
    … 
    case 常量表达式 n:  语句 n;
    default:  语句 n+1;}
    >
    > 意思为先计算表达式的值，再逐个和 case 后的常量表达式比较，若不等则继续往下比较，若一直不等，则执行 default 后的语句；若等于某一个常量表达式，则从这个表达式后的语句开始执行，并执行后面所有 case 后的语句。

## 使用示例

1. 拖入 **输入框** 组件，设置输出变量 inputContent，并添加“标题”与“输入描述”，例：请输入任意数字。如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-1.png)

2. 拖入 **条件（Swtich）** 组件，设置表达式 `Convert.ToInt32(inputContent) + 3 >= 10`:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-2.png)

3. 双击展开条件 Switch 组件，并点击 “Case True”模块，拖入 **写入日志** 组件至容器内，填入当表达式为真的描述：您输入的数字大于或等于 7。用相同的操作设置“Case False”模块：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-3.png)

4. 保存并点击运行流程，查看日志显示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-4.png)