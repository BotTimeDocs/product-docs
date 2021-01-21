# 参数列表

使用参数列表可以创建和修改参数。

![参数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Argument/argumentPanel.png)

|字段 |描述 |
|-----|------|
|名称（必填）| 参数的名称。如果不向参数添加名称，则会自动生成一个名称。 |
|方向（必填） |为参数选择一个方向。可用选项如下：</br> 输入 – 该参数只能用在给定项目；</br> 输出 – 该参数可用于将数据传递到给定项目之外；</br> 输入/输出 – 这些参数可以在给定项目的内部和外部使用；</br> 属性 – 该参数当前尚未使用到。
|参数类型（必填） |选择你希望参数存储的值类型。可用选项如下：</br>- Boolean：布尔 </br>- Int32：32 位整型 </br>- String：字符串型 </br>- Object：对象 </br>- Array of [T] ：数组 </br> - System.Data.DataTable：内存中数据的一个表 </br> - BotTimeUI.Common.Control.Interface.IUiObject </br>- Encoo.DataType.FilePath：打开文件 </br>- Encoo.DataType.FolderPath：打开目录 </br> 浏览 .Net 类型 </br> 如果从“浏览并选择 .Net 类型”窗口中选择 .Net 类型，则会将其添加到“参数类型”下拉框中。 |
|默认值（可选）|参数的默认值。如果此字段为空，则参数没有默认值。 |

> **注意：**
>
> 参数的名称不可使用系统保留字。例如：add、delete 等。

## 参数上下文菜单

![菜单](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Argument/argumentPanelMenu.png)

|字段 |描述 |
|-----|------|
|删除 |将参数从列表中删除，但不从流程中删除。|
|添加批注| 打开“添加批注”窗口，为参数添加注释。 |
|编辑批注| 打开“添加批注”窗口，对已有的注释进行更改。 |
|删除批注| 删除为参数添加的注释。|
