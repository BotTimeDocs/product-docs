# 变量 
在云扩编辑器中，**变量**贯穿于自动化流程的整个过程中，用于存储多种类型的数据。变量另一个关键的方面是它们的值可以改变，以便您可以控制循环体执行的次数。

>注意： 
> 
>即使在不同的作用域中使用，也需要使用不同的名称创建变量。 

存储在变量中的数据称为值，它可以是多种类型。在云扩编辑器中，我们支持大量类型，例如文本、数字、数据表格、时间和日期等等。 

## 创建变量

![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/variabletips.png)

>注意： 
> 
>如果设计窗口没有组件，则无法创建变量。 
  
**从上下文菜单创建变量** 

1、右击当前组件，唤出上下文菜单，单击“创建变量”。 

![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/menu-createVariable.png)

2、填写名称，然后按 Enter 键。您可以在变量面板中查看和编辑它。像这样创建的变量的范围始终属于它所属的最小容器。

>注意： 
> 
>  创建此类变量时，将根据所选属性自动生成类型。 
  
**从变量面板创建变量** 

1、在设计窗口中，单击“变量”，将显示“变量”面板。

![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/variablePanel-createVariable.png)

2、单击“创建变量”，将显示具有默认字段值的新变量。 
>  注意: 
> 
>  默认情况下，如果从“变量面板”创建它们，则所有新变量都是 String 类型。 
  
## 删除变量 
1、在变量面板中，选中一个变量并右击，在上下文菜单中点击“删除”。 

![删除变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/deleteVariable.png)

2、在变量面板中，选择一个变量并按 Delete 键。 
>  注意： 
> 
>  如果要撤消此操作，请按 Ctrl + Z 。 

## 浏览 .Net 变量类型 
要搜索“变量类型”列表中默认未显示的变量类型，请执行以下操作：

1、在变量面板的“变量类型”下拉列表中，选择“浏览类型”。显示“浏览并选择 .Net 类型”窗口。 

![浏览类型](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/viewTypeOfVariable.png)

2、在“类型名称”字段中，输入要查找的变量类型的关键字，例如 table 。

![输入变量类型](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/inputTable.png)

3、选中table类型并单击“确定”。该变量类型将显示在变量面板中。 

![选中类型](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/confirmTable.png)

>  注意： 
> 
>  首次使用“浏览并选择 .Net 类型”窗口中的一种变量类型后，它将显示在变量面板的“变量类型”下拉列表中。 
