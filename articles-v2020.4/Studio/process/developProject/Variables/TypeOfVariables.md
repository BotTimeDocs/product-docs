# 变量类型

如下介绍部分常用的变量类型及使用方法，更多变量的类型及使用可参见[官方文档](https://docs.microsoft.com/zh-cn/dotnet/api/system?view=netframework-4.6.1)。

![变量类型](https://docimages.blob.core.chinacloudapi.cn/images/Studio/datatype20210908.png)

## 布尔型变量

布尔型（Boolean）变量只有两个可能的值，True 或 False 。这些变量通常用来做判断，从而更好地控制流程。如，`result=true`。

## 数值型变量

数值型变量主要分为整数型变量和双精度（小数）型。同时支持数值型的变量之间进行算术运算，常见的算术运算符有：加法运算符（+）、减法运算符（-）、乘法运算符（*）、 除法运算符（/）、余数运算符（%）。

- **整数型变量**

整数型（Int32）变量用于存储数字信息。它们可用于执行方程式或比较，传递重要数据和许多其他数据。如，`num=28`。

- **双精度型变量**

双精度型（Double）变量用于存储浮点类型的小数数据。如，`score=98.4`。

## 字符串型变量

字符串型（String）变量是一种只能存储字符串的变量类型。这些类型的变量可用于存储任何信息，如员工姓名、用户名或任何其他字符串等等。如，`name="Ula"`。

> **注意：**
>
> 云扩 RPA 编辑器中的所有字符串都必须放置在英文引号之间。

## 对象型变量

对象型（Object）变量是一种特殊的变量，可以存储几乎任何类型的数据，例如：整数、字符串、数组等等，如，`obj=100`。

## 日期和时间型变量

日期和时间型（DateTime）变量是一种可用于存储有关任何日期和时间的信息的变量类型，如，`dt=2021/9/8 18:30:00`。

例如，它们可用于将日期附加到你可能正在使用的发票或任何其他文档中，并且对时间敏感。

## Datatable 型变量

DataTable 型变量表示的是一种可以存储大量信息，并充当数据库或包含行和列的简单电子表格的变量类型，如，`table=new DataTable("PrentTable")`。

## 数组型变量

数组型（Array）变量是一种允许你存储多个相同类型的值的变量类型。
云扩 RPA 编辑器支持的数组类型与变量类型一样多。这意味着你可以创建数字数组、字符串数组、布尔值数组等等，如，`topic=new String[]{"a","b"}`。

## 集合型变量

集合型（List）变量是 C#编程中的经常使用的集合之一，相对数组它可以动态的添加元素而不是声明的时候就必须指定大小。如，`testList=new List<string>{"a","b","c"}`。

## 字典型变量

字典型（Dictionary）变量表示键和值的集合。它本身有集合的功能有时候可以把它看成数组。如，`testDictionary=new Dictionary<Int32,Int32>()`

## 云扩自定义的变量

如下为云扩在针对特定场景专门定制的变量类型，一般用于 [参数](./../Arguments/Arguments.md) 中：

![参数类型](https://docimages.blob.core.chinacloudapi.cn/images/Studio/arguments20210909.png)

- **Encoo.DataType.FoderPath**：文件夹路径，可视化界面选择文件夹路径，无需手动填写。
- **Encoo.DataType.FilePath**：文件路径，可视化界面选择文件路径，无需手动填写。
- **Encoo.DataType.Password**：密码，输入密码时非明文显示。
- **BotTimeUI.Common.Control.Interface.IUiObject**：用于自动化组件的“控件元素”属性中接收结果。

这些变量对于将特定数据从数据库迁移到另一个数据库、从网站提取信息并将其本地存储在电子表格和许多其他文件中时是非常有用的。
