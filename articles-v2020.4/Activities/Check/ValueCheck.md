# 值校验

## 视频示例

## 概述

将两个值进行对比，根据对比条件返回布尔值

可使用此种方法取得元素的属性值：IUiObject.**GetProperty**(“attributeName”).toString()

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **期望值** ：进行对比的值。仅支持字符串变量和字符串
- **实际值** ：进行对比的值。仅支持字符串变量和字符串
- **校验模式** ：对实际值和期望值进行对比的模式，例如等于，大于，小于等，可通过下拉框选择

    > **说明：**
    >
    > 如下列出较难理解的校验符号。
    > - 开始于：确定字符串是否以指定字符串的字符开头，返回 true 或 false。
    > - 结束于：确定字符串是否以指定字符串的字符结束，返回 true 或 false。

### 输出

- **结果** ：输出两个值对比后的 Boolean 类型结果

## 使用示例

1. 拖入 **值校验** 组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/valueCheck-1.png)

2. 以校验模式为“开始于”举个例子，设置期望值为“a”，实际值为 "abc"，设置变量“flag”输出两个值对比后的 Boolean 类型结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/valueCheck-2.png)

3. 拖入 **写入日志** 组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/valueCheck-3.png)

4. 运行流程，控制台输出两个值对比后的 Boolean 类型结果，如，“True”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/valueCheck-4.png)
