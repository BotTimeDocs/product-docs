# 写入区域

写入数据表数据到工作表

##  属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


输入

- **数据表** ：写入工作表内的数据表数据。可传入&quot;读取区域&quot;的输出变量，实现复制粘贴效果。仅支持数据表变量

目标

- **开始单元格** ：数据表数据开始写入的单元格地址。若为单元格地址，则从指定单元格为起始写入数据表；若为单元格区域，则只填充数据到指定区域。仅支持字符串变量和字符串
- **工作表** ：写入数据表数据的目标工作表。若指定工作表不存在则自动新建。仅支持字符串变量和字符串

可选项

- **添加列头** ：勾选时，数据表列头也将写进工作表
## 操作样例

1. 拖入**打开/新建**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击**...**选择本地Excel文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入**读取区域**组件至项目流程中，填写sheet名称“sheet1”，填写读取区域范围“A1：D3”，新建变量"datatable"类型为datatable，用来存放区域内所有单元格的内容
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadRange1.png)

4. 拖入**写入区域**组件至项目流程中，填写sheet名称“sheet2”，填写写入区域范围“A1：D3”，填写要写入的变量，这里使用"datatable"。也就是使用“sheet1”的“A1：D3”的内容写入“sheet2”的“A1：D3”
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadRange2.png)

5. 点击运行，运行成功后。打开Excel查看A1的内容已经写入A2。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadRange3.png)