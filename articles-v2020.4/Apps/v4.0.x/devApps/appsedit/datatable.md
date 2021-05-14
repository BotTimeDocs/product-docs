# 数据表

数据表是以行形式展示的表格形式的信息，用户可以在数据源中通过开发引用该表来显示并操作表数据。

## 新增/导入数据表

- **新增数据表**

1. 进入 ViCode 应用的开发模式，选择“数据表 > 新建表”。

    ![新增数据表](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/newdatatable20210511.png)

2. 在弹出的“创建数据表”弹框中，按需填写数据表信息。

   - **表格名称**：自定义数据表名称。
   - **备注**：为自定义的表格名称添加描述类信息。
   - **连接器名称**：自定义连接器名称。
   - **开发环境**：下拉选择环境类型，支持开发环境和生产环境。

    ![创建数据表](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/newdatatabledemo20210511.png)

3. 单击“确定”按钮，完成数据表的创建，在左侧数据表列表中可查看。

- **导入数据表**

1. 进入 ViCode 应用的开发模式，选择“数据表 > 导入表”。

    ![导入数据表](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/importdatatable20210511.png)

2. 在弹出的“打开”文件对话框中，选择需要导入的数据表。

    > **说明：**
    >
    > 需要导入的数据表可以是已导出的数据表，也可以是自定义的 excel 或 csv 格式的表格文件。

    ![选择需要导入的数据表](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/selectimportdatatable20210511.png)

3. 单击“打开”，在页面右上角会出现 "导入成功" 提示。

## 数据表的基本操作

数据表的基本，包括对已创建完成的数据表进行数据表名的增、删、改、查，以及对数据表进行授权等操作。

### 搜索数据表

在数据表列表上方的搜索框中，输入数据表名称进行搜索数据表。

![搜索数据表](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/searchdatatable20210511.png)

### 修改数据表名

右击需要修改的数据表，选择“重命名”选项，可对数据表进行重命名。

![修改数据表名](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/editdatatable20210511.png)

### 查看数据表基本信息

单击数据表页面中的“基本信息”选项，可查看已创建的数据表的基本信息。

![查看数据表基本信息](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/viewdatatableinfo20210511.png)

### 管理配置数据表权限

单击数据表页面中的“权限管理”选项，可对当前数据表进行权限设置。

![管理数据表权限](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/datatableprivage20210511.png)

### 删除数据表

- 方法一：选择需要删除的数据表，单击数据表列表右上方的“删除”图标，可删除当前数据表。

    ![删除数据表](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/deletedatatable20210511.png)

- 方法二：选择需要删除的数据表，右击选择“删除”选项，可删除当前数据表。
  
    ![删除数据表](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/deletedatatable220210511.png)

## 表数据操作

表数据操作包括对已创建数据表中的数据进行编辑及设置等操作。

### 新增行/列

- 方式一：通过单击表格中最底端和最右端的 " 新增”图标，可在末行或末列增加一个空行或空列。

- 方式二：通过在表格中右击菜单选择“插入行”或“插入列”选项，可插入一个空行或空列。

![新增行/列](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/insertcolumnrow20210511.png)

### 复制粘贴行/列

当需要复制某个单元格或某个区域的内容时，可选择需要复制的区域右击选择“复制”选项，到需要粘贴的区域右击选择“粘贴”选项。

> **说明：**
>
> 也可以直接使用快捷键 Ctrl+C 复制和 Ctrl+V 粘贴。

![复制粘贴行/列](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/copypaste20210511.png)

### 调整列宽

通过拖拽列间的表格线，可调整该列的宽度。

![调整列宽](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/dragwidth20210511.png)

### 拖拽覆盖单元格数据

选择单元格，当光标变成上下左右箭头时，可向上下左右进行拖动时，可覆盖原单元格中的内容。

![覆盖单元格数据](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/dragunit20210511.png)

### 多选操作行

当需要选择多行或多列时，可按住 Shift 键，同时按下需要选择的单元格，可进行多选操作行。

![多选操作行](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/muliselect20210511.png)

### 设置列格式

- 方式一：选择单元格或列，单击“设置列格式”选项，可对单元格或某列的值设置数据格式。

- 方式二：选择单元格或列，右击选择“设置列格式”选项，可对单元格或某列的值设置数据格式。

![设置列格式](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/setcolumnformat20210511.png)

目前支持的数据格式分类，如下图所示：

![数据格式分类](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/columntype20210511.png)

### 筛选/排序数据记录

单击表头字段右侧的倒立的小三角，在弹出的框中，可对当前列进行排序和筛选操作。

- 排序：支持按升序/降序对数据记录进行排序。
- 筛选：支持按“值”或“条件”进行筛选数据记录。

![筛选排序数据记录](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/filtersort20210511.png)

### 删除行/列

选择单个单元格或一行数据，右击选择“删除”选项，可按需删除对应的行或列。

![删除行/列](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/deletecolumnrow20210511.png)

### 导出 Excel/CSV

已创建完成的数据表，通过点击数据表页面中的“导出表格”选项，可按需导出 Excel 或 CSV 类型的文件。

![导出表格](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/exporttable20210511.png)
