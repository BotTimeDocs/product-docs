# 自动填充

从源单元格区域自动填充数据到目标区域。此组件仅可在&quot;打开/新建&quot;组件中使用，默认取其工作簿，无需再次输入

##  属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


输入

- **工作表** ：执行填充操作的目标工作表。若指定工作表不存在则报错。仅支持字符串变量和字符串
- **填充区域** ：欲将源数据自动填充的目标区域
- **源区域** ：进行填充操作的源单元格区域

## 操作样例

1. 拖拽**打开/新建**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击**...**选择本地Excel文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖拽**自动填充**到**打开/新建**组件中，填写sheet名称，填写源区域"A1:C3"。填充区域，请注意支持横向填充"A1:I3"，或者是纵向填充"A1:C9",必须包含源区域，不支持同时横向和纵向填充：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AutoFillRange1.png)

4. 点击运行，运行成功。打开Excel，横向填充成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AutoFillRange2.png)