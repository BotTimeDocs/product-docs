# 数据表编辑模式
数据表编辑模式页面主要提供对数据表内的数据进行的排序、筛选、设置格式等操作，像操作 Excel 一样操作小程序的数据表。

![数据表详情](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/tabledetail20201207.png)
<br>

## 数据表操作

- **重合名表名**：右击数据表名称，在弹出的菜单中选择“重命名”，即可对表名进行重命名。
![重命名表名](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/rename20201207.png)
<br>

- **删除表名**：右击数据表名称，在弹出的菜单中选择“删除”，即可对当前表进行删除。
![删除表名](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/deletetablename20201207.png)
<br>
- **退出编辑模式**：单击数据表名上方的“退出编辑”链接，即可退出编辑模式，返回至数据表管理列表页面。
![退出编辑模式](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/exitedit20201207.png)
<br>

## 数据表内容操作
- **插入行/列**
  - 方式一：单击表格行/列末端的![新增行/列](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/addcolum20201207.png)图标。
  - 方式二：选中单个表格/列/全表，在右击菜单中选择并单击**插入行/列**菜单进行选择需要插入行/列的位置。

  ![插入行/列](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/addline20201207.png)
  <br>

- **修改表数据**
将光标置于需要修改的表的单元格内，进行输入表数据。
<br>

- **复制/粘贴单元格**
选中表中的部分数据，右击选择“复制”，光标移至需要粘贴的地方，右击选择“粘贴”。
  >**说明：**
  >按住Shift键+光标选择，可多选单元格进行删除或复制操作。 

  ![复制/粘贴单元格](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/copycaste20201207.png)
<br>

- **扩展数据至范围**
选中单个单元格数据，拖拽单元格右下角的光标可横向或纵向覆盖原有单元格数据为当前选中的单个单元格中的数据。
![扩展数据至范围](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/extend20201207.png)
<br>

- **筛选表数据**
  - 单击表格中表头字段右侧的倒三角图标，支持按值或条件进行筛选数据。
  ![筛选列数据](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/filterdata20201207.png)
  <br>
  
  - 在单元格中引用数组形式的数据，可预览已筛选数据。
  ![筛选单元格数据](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/filtercell20201207.png)
  <br>


- **排序表数据**
  - **列排序**：单击表格中表头字段右侧的倒三角图标，支持按升序、降序或不排序对数据进行排序。
 
    ![排序表数据](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/sort20201207.png)
<br>

  - **拖拽排序**：选中任一需要移动的行/列，拖动至需要移至的行/列处。

    ![表头字段排序](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/movesort20201208.png)
<br>


- **设置列格式**
  - 方式一：选中整列或单个单元格，右击选择**设置列格式**。在弹出的列设置弹窗中按需进行设置。
  - 方式二：选中整列或单个单元格，单击上方**设置列格式**按钮。在弹出的列设置弹窗中按需进行设置。
  >**说明：**
  >
  > 仅支持列格式配置，不支持单个单元格格式配置。
   
  ![设置列格式](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/setcoulm20201207.png)

<br>

- **应用公式到单元格**
选中单个表格/列/全表，显示当前选中项的值/公式。单元格中支持的公式，可参见[公式列表](https://formulajs.info/functions/)。
![应用公式到单元格](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/folum20201207.png)
<br>

- **导出表格**
单击上方的“导出”按钮，将当前表导出为 xlsx 或 csv 格式并自动下载至本地电脑。
![导出表格](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/exportexcel20201207.png)