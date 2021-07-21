# 属性校验

## 视频示例

## 概述

适用于对界面某一元素的属性值进行判断。可以通过指定元素的方式，自动生成选择器属性，其后只需选择 **属性名** 属性，例如“Id”等即可。最终将取“属性名”和“值”进行对比，根据对比条件返回布尔值。

>**说明：**
>
>属性名下拉框中仅显示当前元素支持的属性。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。

### 目标

- **控件元素** ：通过属性来定位元素，并取此元素的值进行校验。变量类型为IUiObject。此属性和选择器属性两者互斥且必选一填写
- **匹配超时(毫秒)** ：查找选择器或控件元素所指定元素的时间，毫秒为单位。若超过此时间还未匹配到指定元素则会抛出错误。仅支持整型变量和整型
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：要进行属性校验的元素的选择器表达式，可通过“指定元素”自动生成，同时可支持修改。此属性和控件元素属性两者互斥且必选一填写

### 输入

- **属性名** ：要比较的元素的属性名。浏览器端不区分大小写，桌面端首字母应大写。仅支持字符串变量和字符串
  
  >**说明：**
  >
  >支持在组件中属性名的下拉列表框中输入已存在但未显示的自定义属性。

- **值** ：与指定元素的属性值进行对比的值。仅支持字符串变量和字符串
- **校验模式** ：对元素属性值和值进行对比的模式，例如等于，大于，小于等，可通过下拉框选择

### 输出

- **结果** ：将两个值对比后的结果保存到此变量

  >**说明：**
  >
  >HTML返回 tagName属性的值为大写。

## 使用示例

1. 拖入**属性校验**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/attributeCheck-1.png)

2. 以校验模式为“=”举个例子，设置属性名为“url”，值为"https://www.baidu.com/ ”，设置变量“flag”来输出两个值对比后的Boolean类型结果，选择器通过“指定元素”自动生成：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/attributeCheck-2.png)

3. 拖入**写入日志**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/attributeCheck-3.png)

4. 运行流程，控制台输出两个值对比后的Boolean类型结果，如，“True”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/attributeCheck-4.png)




