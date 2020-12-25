# 读取单元格

获取工作簿单元格内数据并可存储在变量中

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


输入

- **工作表** ：目标单元格所在工作表。仅支持字符串变量和字符串
- **单元格** ：读取数据的目标单元格。仅支持字符串变量和字符串

输出

- **数据** ：将读取到的目标单元格内数据存储在此变量内

可选项

- **保留格式** ：勾选时，将同时读取目标单元格的数据内容和数据格式（例如：货币，日期等），并在作为&quot;写入单元格&quot;的输入时，同时保持此数据格式；不勾选时，在&quot;写入单元格&quot;时使用默认&quot;常规&quot;数据格式
## 操作样例

1. 拖入**打开/新建**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击**...**选择本地Excel文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入**读取单元格**组件至项目流程中，填写sheet名称，填写单元格名称，新建变量"cellContent"类型为String，用来存放单元格内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCell1.png)

4. 拖入**写入单元格**组件至项目流程中，填写sheet名称，填写单元格名称，填写要写入的变量，这里使用"cellContent"。也就是使用A1的内容写入A2：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCell2.png)

5. 点击运行，运行成功后打开Excel查看A1的内容已经写入A2：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCell3.png)
