# 执行宏

## 视频示例

## 概述

执行外部宏文件或者 XLSM 格式的内部宏，支持实参传递

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **Sub/Function 名** ：执行宏的方法名。内部宏和外部宏均需填充此项。仅支持字符串变量和字符串
- **传入实参** ：传入宏文件的实参
- **宏文件路径** ：执行此外部宏文件。为空时，默认执行工作表内部宏

### 输出

- **返回值** ：将宏执行后返回的值存储在此变量，前提为执行宏后有返回值

## 使用示例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **执行宏** 组件到 **打开/新建** 组件中，选择宏文件路径，填写方法名 "GetFirstNSheetNames"，定义 Object 类型的变量 "names"，传入实参“new List <Object> {6}”，填写返回值 names：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExecuteMacro1.png)

5. 拖拽 **循环操作（For Each）** 到 **打开/新建** 组件中，拖拽 **写入日志** 到 **循环操作（For Each）** 组件中，填入转换后的变量“(string [])names”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExecuteMacro2.png)

6. 运行成功后，日志打印所有 sheet 名称。

附宏文件供参考：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExecuteMacro3.png)

