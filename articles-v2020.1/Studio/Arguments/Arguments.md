# 参数 
**参数**用于将数据从项目传递到另一个项目。在全局意义上，它们类似于变量，因为它们动态地存储数据并将其传递。变量在组件之间传递数据，而参数在自动化流程之间传递数据。因此，它们使你能够一次又一次地重用自动化流程。 

云扩编辑器支持大量的参数类型，这些参数类型与变量类型一致。因此，你可以创建字符串型，布尔值型，对象型，数组型或 DataTable 型参数，也可以浏览 .Net 类型，和在变量的情况下一样。 

此外，参数具有特定的传递方向（输入，输出，输入/输出，属性），告诉应用程序存储在其中的信息应该传递到哪里。

## 创建参数 
>注意： 
> 
>参数名称应在驼峰上用一个前缀，说明参数传递的方向。 
> 
>如 in_DefaultTimeout，in_FileName，out_TextResult，io_RetryNumber。

要创建新参数： 

1. 在“设计窗口”中，点击“参数”。将显示参数面板。 

    ![创建参数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Argument/argumentPanel-createArgument.png)

2. 点击“创建参数”行。将显示具有默认字段值的新参数。 

>注意：   
> 
>默认情况下，所有参数都是输入方向的字符串 (String) 类型。  

## 删除参数 
1.  在参数面板中，选中一个参数并右击，在上下文菜单中点击“删除”选项。 

    ![删除参数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Argument/deleteArgument.png)

2. 在参数面板中，选择一个参数并按 Delete 。 

>  注意： 
> 
>  如果要撤消此操作，请按 Ctrl + Z 。 

