# 变量 
在云扩RPA编辑器中，**变量**贯穿于自动化流程的整个过程中，用于存储多种类型的数据。变量另一个关键的方面是它们的值可以改变，以便你可以控制循环体执行的次数。

>注意： 
> 
>即使在不同的作用域中使用，也需要使用不同的名称创建变量。 

存储在变量中的数据称为值，它可以是多种类型。在云扩RPA编辑器中，我们支持大量类型，例如文本、数字、时间和日期等等。 

## 创建变量

![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/variabletips.png)

>注意： 
> 
>如果编辑区域没有组件，则无法创建变量。 

### 快捷键 Ctrl+B 创建变量

**从组件中** 

1. 从组件面板拖入一个组件到编辑区域。在组件的输入框中填入变量名称。
2. 选中名称并右击，从上下文菜单中选择“创建变量”，或者使用快捷键 **Ctrl+B** ，将创建该变量。通过变量列表可检查变量的类型和范围。

   ![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/Activity-createVariable.png)

**从属性面板中**

1. 在任一组件的属性面板中，选择某一属性，在输入框中填入变量名称。
2. 选中名称并右击，从上下文菜单中选择“创建变量”，或者使用快捷键 **Ctrl+B** ，将创建该变量。通过变量列表可检查变量的类型和范围。

   ![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/Property-createVariable.png)

**从表达式编辑器中**

1. 选择任一组件，打开该组件某一属性的表达式编辑器，填入一段表达式。
2. 选择表达式的一部分并右击，从上下文中选择“创建变量”，或者使用快捷键 **Ctrl+B** ，将创建该变量。通过变量列表可检查变量的类型和范围。

   ![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/Editor-createVariable.png)

>注意： 
> 
>  通过快捷键创建的变量将根据所选属性自动生成类型。 
  
### 从上下文菜单创建变量

1. 右击当前组件，唤出上下文菜单，点击“创建变量”。 

   ![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/menu-createVariable.png)

2. 填写名称，然后按 Enter 键。你可以在变量列表中查看和编辑它。像这样创建的变量的范围始终属于它所属的最小容器。

>  注意: 
> 
>  默认情况下，通过上下文菜单创建的变量都是 String 类型。 
  
### 从变量列表创建变量

1. 在编辑区域中，点击“变量”，将显示“变量”列表。

   ![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/variablePanel-createVariable.png)

2. 点击“创建变量”，将显示具有默认字段值的新变量。 

>  注意: 
> 
>  默认情况下，如果从“变量列表”创建它们，则所有新变量都是 String 类型。 
  
## 删除变量 
1. 在变量列表中，选中一个变量并右击，在上下文菜单中点击“删除”。 

   ![删除变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/deleteVariable.png)

2. 在变量列表中，选择一个变量并按 Delete 键。 

>  注意： 
> 
>  如果要撤消此操作，请按 Ctrl + Z 。 

## 浏览 .Net 变量类型 
要搜索“变量类型”下拉框中默认未显示的变量类型，请执行以下操作：

1. 在变量列表的“变量类型”下拉框中，选择“浏览类型”。显示“浏览并选择 .Net 类型”窗口。 

    ![浏览类型](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/viewTypeOfVariable.png)

2. 在“类型名称”字段中，输入要查找的变量类型的关键字，例如 table 。

    ![输入变量类型](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/inputTable.png)

3. 选中table类型并点击“确定”。该变量类型将显示在“变量类型”下拉框中。 

    ![选中类型](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/confirmTable.png)

>  注意： 
> 
>  首次使用“浏览并选择 .Net 类型”窗口中的一种变量类型后，它将显示在变量列表的“变量类型”下拉框中。 
