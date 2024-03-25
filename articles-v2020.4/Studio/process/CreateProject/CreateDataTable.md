# 创建数据表

## 什么是数据表
数据表是一个保存临时数据的表格，可以理解为一个临时的Excel表格或数据库，当流程中需要使用时可以直接调用。
</br></br>
> 需要注意数据表存储的是临时数据，当流程运行结束后运行中做的改动均会被销毁，如果需要保存处理的数据，需要使用[保存为Excel](null)或[保存至控制台数据表](null)等组件进行操作。
</br> 

## 怎样创建数据表 

### 在项目中创建数据表

右键点击项目目录下的数据表，之后点击“新建数据表”
</br>

![编辑器创建](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt001.png)
</br>

在弹出的窗口中输入数据表名称后点击“确定”按钮完成数据表的创建
</br>

![新建窗口](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt002.png)
</br>

之后根据提示点击“重新加载项目”即可完成数据表创建
</br>

![重新加载项目](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt003.png)
</br>

>项目中创建的数据表是在流程执行前创建，可以添加初始的数据，在流程运行结束后会还原为初始状态。

### 通过组件创建数据表
也可以使用组件“[搭建数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/BuildDataTable.md?_v=v2020.1)”创建流程中存储临时数据的数据表。
</br>

>通过组件创建数据表会在流程运行之后再创建数据，在流程运行结束后销毁。

### 通过控制台创建数据表
登录控制台之后进入“数据中心”的“数据表管理”中，点击“新建”按钮

![控制台](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt0013.png)
</br>

输入“数据表名称”和“备注”后点击“确定”即可完成创建。

![控制台新建](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt0014.png)
</br>

导入控制台数据表参见 [导入控制台数据表](#3--导入控制台数据表)
</br>

>控制台创建的数据表暂不支持直接创建数据，如需存储数据可使用

## 如何添加数据
1. ### 通过界面创建
   双击打开创建的数据表后点击数据表页签中的“编辑列”->之后点击“添加列”->在弹窗中编辑要创建的列类型->点击确认即可完成列的创建。
   </br>
   ![创建数据表](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt005.png)

   **列的属性包括：**
   </br>
   **列名**：创建数据表列的名称
   </br>
   **数据类型**：设置该列的数据类型，支持String、int32、Double、Boolean、DateTime、Object这些常规数据类型；
   </br>
   **默认值**：设置该列新添加数据时的初始值
   </br>
   **唯一值**：设置该列是否限制填入数据唯一性，选中时填入的值不可重复；
   </br>
   **值可为空**：设置该列是否运行空值，选中时允许为空；
   </br>
   **整形自动加一**：当该列数据类型为int32时新添加的值是否自动加一，选中时自动加一；
   </br>
   **最大长度**：当该列数据类型为String类型时是否限制最大长度，默认为不限制；
   </br>

   之后点击行选中，再点击“删除列”即可删除当前选中的列及其中的数据；点击“上移”或“下移”来切换列的排序；也可以点击列的属性进行修改。
   </br>

   ![列按钮](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt007.png)

   创建列之后点击“添加行”，在弹出的弹窗中添加数据后点击“确定”即可在数据表中添加数据

   ![添加行](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt006.png)
   </br>
   之后点击行选中，再点击“删除行”即可删除当前选中的行及其中的数据；点击“清空数据”以删除整张表内的全部数据；选中行后双击可以修改数据。

   ![行按钮](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt008.png)
   </br>
    修改数据后点击“保存数据表”或使用快捷键*Ctrl+S*保存编辑的数据。</br>
    ![保存按钮](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt0015.png)

    >添加列支持 

2. ### 导入Excel文件
   
   点击“导入数据表”->选择“Excel”

   ![导入数据表](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt009.png)
   
   在弹窗中选择Excel文件->编辑要导入的工作表名->点击“确定”完成导入
   
   ![导入弹窗](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt0010.png)

   >导入的Excel支持.xls、.xlsx、.et、.ett格式的文件

3. ### 导入控制台数据表
   点击“导入数据表”->之后选择“控制台”

   ![导入控制台](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt0011.png)
   </br>
   在弹出的弹窗中选择“部门”和“数据表”后点“确定”即可导入控制台数据表。

   ![控制台弹窗](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt0012.png)

   >导入控制台数据表前需确保编辑器已登录到控制台、在控制台中对应的部门下已创建数据表并且该拥有该表操作权限 

4. ### 导入CSV及其他文件
   如需导入CSV文件数据，可以在流程中使用组件[读取CSV文件](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/ReadCSV.md?_v=v2020.1)

   如需读取Excel中特定区域的数据，可以在流程中使用Excel组件[读取区域](https://academy.encoo.com/zh-cn/wiki/Activities/TableExcelWPS/ReadRange.md?_v=v2020.1)


>组件创建的数据表是在流程运行后生成，无法导入到数据表中，如需使用可在流程运行中直接使用组件输出的DataTable变量；</br>
>当数据表内已有数据时再导入数据会提示是否覆盖，覆盖后原有的数据会被销毁。

## 怎样使用数据表
1. 数据表需要通过数据表组件使用。需要使用项目路径下创建的数据表时，在组件中以 **Project.DataTableName** 的方式进行引用，如创建了数据表“DataTable1”，则在需要使用DataTable类型的组件中输入 **Project.DataTable1**.

   ![控制台弹窗](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt004.png)

2. 控制台创建的数据表需要使用组件[读取控制台数据表]()读取后直接在组件中使用输出的DataTable类型变量，如创建了DataTbale类型的变量DataTable1，在组件中直接输入DataTable1即可

   ![控制台弹窗](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/dt0016.png)

3. 组件创建的数据表同控制台数据表使用方式一样，直接使用组件输出的DataTable类型变量即可。

## 怎样保存数据表中的数据

1. 需要将数据保存到Excel中可以使用组件[保存为Excel文件]()或[追加到Excel文件]()

2. 需要将数据保存到CSV中可以使用组件[保存为CSV文件]()或[追加到CSV文件]()

3. 需要将数据保存到控制台中可以使用组件[保存到控制台数据表]()或[追加到控制台数据表]()

## 数据表组件
[搭建数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/BuildDataTable.md?_v=v2020.1)
</br>
[预览数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/PreviewDataTable.md?_v=v2020.1)
</br>
[输出数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/OutputDataTable.md?_v=v2020.1)
</br>
[清空数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/ClearDataTable.md?_v=v2020.1)
</br>
[合并数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/MergeDataTable.md?_v=v2020.1)
</br>
[联结数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/JoinDataTable.md?_v=v2020.1)
</br>
[添加数据行](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/AddRow.md?_v=v2020.1)
</br>
[添加数据列](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/AddColumn.md?_v=v2020.1)
</br>
[移除行](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/RemoveRow.md?_v=v2020.1)
</br>
[移除列](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/RemoveColumn.md?_v=v2020.1)
</br>
[移除重复行](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/RemoveDuplicateRow.md?_v=v2020.1)
</br>
[遍历行](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/ForEachRow.md?_v=v2020.1)
</br>
[排序](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/SortDataTable.md?_v=v2020.1)
</br>
[筛选](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/FilterDataTable.md?_v=v2020.1)
</br>
[获取单元格的值](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/GetValue.md?_v=v2020.1)
</br>
[设置数据表的值](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/DataTableSetValue.md?_v=v2020.1)
</br>
[设置数据行的值](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/DataRowSetValue.md?_v=v2020.1)
</br>
[保存为CSV文件](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/SaveToCSV.md?_v=v2020.1)
</br>
[读取CSV文件](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/ReadCSV.md?_v=v2020.1)
</br>
[追加到CSV文件](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/AppendToCSV.md?_v=v2020.1)
</br>
[读取Excel文件](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/ReadFromExcel.md?_v=v2020.1)
</br>
[保存为Excel文件](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/AppendToCSV.md?_v=v2020.1)
</br>
[追加到Excel文件](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/SaveToExcel.md?_v=v2020.1)
</br>
[读取控制台数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/ReadConsoleDT.md?_v=v2020.1)
</br>
[保存至控制台数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/SaveConsoleDT.md?_v=v2020.1)
</br>
[追加到控制台数据表](https://academy.encoo.com/zh-cn/wiki/Activities/DataProcessing/DataTable/AppendConsoleDT.md?_v=v2020.1)

## 常见问题
1. **运行流程后流程中操作的数据表数据为什么没有了**</br>
   数据表保存的是临时数据，在流程终止后销毁，如需保存相关数据，可参见[怎样保存数据表中的数据](##怎样保存数据表中的数据)
2. **数据表处理数据的限制是什么**</br>
   在流程中处理数据时无限制，当需要进行存储时会受到文件本身的规则限制，如Excel只能打开小于65537行的CSV文件，上传到控制台数据表时限制为必须小于**20M**，并且要小于**65537**行和**128**列。
