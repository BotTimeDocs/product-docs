# 写入行/列数据

横向或纵向写入数据到工作表中，支持自定义起始单元格地址执行写入

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


输入

- **写入行/列** ：写入数据的模式选择（横向写入数据或纵向写入数据）。选择&quot;横向写入数据&quot;后，则取用户指定的起始单元格地址，开始横向写入数据；选择&quot;纵向写入数据&quot;后，则取用户指定的起始单元格地址，开始纵向写入数据
- **数据** ：写入工作表内的数据，例如：new object[]{"value1","value2","value3"} 向指定的行/列插入3个值value1,value2,value3


目标

- **工作表** ：写入数据的目标工作表。若指定工作表不存在则自动新建。仅支持字符串变量和字符串
- **起始单元格** ：写入数据的开始单元格地址。仅支持字符串变量和字符串

## 操作样例

1. 拖入**打开/新建**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击**...**选择本地Excel文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入**读取行/列数据**组件至项目流程中，填写sheet名称“sheet1”，填写起始单元格“A1”，新建变量"row"类型为Object[]用来存放本**行**所有单元格的内容，读取行/列默认选择行：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadRowOrColumn1.png)

4. 拖入**读取行/列数据**组件至项目流程中，填写sheet名称“sheet1”，填写起始单元格“A1”，新建变量"col"类型为Object[]用来存放本**列**所有单元格的内容，读取行/列选择列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadRowOrColumn2.png)

5. 拖入**写入行/列数据**组件至项目流程中，填写sheet名称“sheet2”，填写起始单元格“A1”，填写类型为Object[]变量"row"用来填充本**行**内容，读取行/列默认选择行：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/WriteRowOrColumn1.png)

6. 拖入**写入行/列数据**组件至项目流程中，填写sheet名称“sheet2”，填写起始单元格“A1”，填写类型为Object[]变量"col"用来填充本**列**内容，读取行/列默认选择列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/WriteRowOrColumn2.png)

7. 点击运行，运行成功后。打开Excel 查看Sheet1第一行的内容从A1开始已经写入sheet2的第一行，Sheet1第一列的内容从A1开始已经写入sheet2的第一列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/WriteRowOrColumn3.png)
