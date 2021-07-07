# 读取行/列数据

读取指定工作表中的某一列或某一行，将读取到的内容保存在数组中并可输出

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 可选项

- **保留格式**：勾选时，将同时读取目标单元格的数据内容和数据格式（例如：货币，日期等），并在作为 "写入单元格" 等写入组件的输入时，同时保持此数据格式；不勾选时，在写入时使用默认 "常规" 数据格式

### 输入

- **读取行/列** ：指定组件操作为读取行或者为读取列。该选项为下拉选框（行，列），默认为行
- **工作表** ：读取的目标行或列所在的工作表。仅支持字符串变量和字符串
- **起始单元格** ：读取行或列时的起始单元格。将从此单元格开始，结合“读取行/列”属性所选择的行或列，来横向或者竖向读取数据。仅支持字符串变量和字符串

### 输出

- **数组** ：将读取到的数据存储在此变量

## 操作样例

1. 拖入 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入 **读取行/列数据** 组件至项目流程中，填写 sheet 名称“sheet1”，填写起始单元格“A1”，新建变量 "row" 类型为 Object [] 用来存放本 **行** 所有单元格的内容，读取行/列默认选择行：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadRowOrColumn1.png)

4. 拖入 **读取行/列数据** 组件至项目流程中，填写 sheet 名称“sheet1”，填写起始单元格“A1”，新建变量 "col" 类型为 Object [] 用来存放本 **列** 所有单元格的内容，读取行/列选择列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadRowOrColumn2.png)

5. 拖入 **写入行/列数据** 组件至项目流程中，填写 sheet 名称“sheet2”，填写起始单元格“A1”，填写类型为 Object [] 变量 "row" 用来填充本 **行** 内容，读取行/列默认选择行：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/WriteRowOrColumn1.png)

6. 拖入 **写入行/列数据** 组件至项目流程中，填写 sheet 名称“sheet2”，填写起始单元格“A1”，填写类型为 Object [] 变量 "col" 用来填充本 **列** 内容，读取行/列默认选择列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/WriteRowOrColumn2.png)

7. 点击运行，运行成功后。打开 Excel 查看 Sheet1 第一行的内容从 A1 开始已经写入 sheet2 的第一行，Sheet1 第一列的内容从 A1 开始已经写入 sheet2 的第一列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/WriteRowOrColumn3.png)
