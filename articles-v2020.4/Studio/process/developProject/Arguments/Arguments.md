# 参数

## 概述

**参数** 用于将数据从项目传递到另一个项目。在全局意义上，它们类似于变量，因为它们动态地存储数据并将其传递。变量在组件之间传递数据，而参数在自动化流程之间传递数据。因此，它们使你能够一次又一次地重用自动化流程。

云扩 RPA 编辑器支持大量的参数类型，这些参数类型与变量类型一致。因此，你可以创建字符串型，布尔值型，对象型，数组型或 DataTable 型参数，也可以浏览 .Net 类型，和在变量的情况下一样。

此外，参数具有特定的传递方向（输入，输出，输入/输出，属性），告诉应用程序存储在其中的信息应该传递到哪里。

## 创建参数

1. 在“编辑区域”中，点击“参数”。将显示参数列表。

    ![创建参数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Argument/argumentPanel-createArgument.png)

2. 点击“创建参数”行。将显示具有默认字段值的新参数。

    > **注意：**
    >
    > 默认情况下，所有参数都是输入方向的字符串 (String) 类型。  

3. 根据如下说明，自定义参数。

    |字段 |描述 |
    |-----|------|
    |名称（必填）| 参数的名称。如果不向参数添加名称，则会自动生成一个名称。 |
    |方向（必填） |为参数选择一个方向。可用选项如下：</br> 输入 – 该参数只能用在给定项目；</br> 输出 – 该参数可用于将数据传递到给定项目之外；</br> 输入/输出 – 这些参数可以在给定项目的内部和外部使用；</br> 属性 – 该参数当前尚未使用到。
    |参数类型（必填） |选择你希望参数存储的值类型。可用选项如下：</br>- Boolean：布尔 </br>- Int32：32 位整型 </br>- String：字符串型 </br>- Object：对象 </br>- Array of [T] ：数组 </br> - System.Data.DataTable：内存中数据的一个表 </br> - BotTimeUI.Common.Control.Interface.IUiObject </br>- Encoo.DataType.FilePath：打开文件 </br>- Encoo.DataType.FolderPath：打开目录 </br> 浏览 .Net 类型 </br> 如果从“浏览并选择 .Net 类型”窗口中选择 .Net 类型，则会将其添加到“参数类型”下拉框中。 |
    |默认值（可选）|参数的默认值。如果此字段为空，则参数没有默认值。 |

    > **注意：**
    >
    > - 参数的名称不可使用系统保留字。例如：add、delete 等。
    > - 参数名称应在驼峰上用一个前缀，说明参数传递的方向。如， `in_DefaultTimeout`，`in_FileName`，`out_TextResult`，`io_RetryNumber`。

## 删除参数

1. 在参数列表中，选中一个参数并右击，在上下文菜单中点击“删除”选项。

    ![删除参数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Argument/deleteArgument.png)

2. 在参数列表中，选择一个参数并按 Delete 。

    > **注意：**
    >
    > 如果要撤消此操作，请按 Ctrl + Z 。
