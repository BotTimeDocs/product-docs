# 获取末行号

获取工作表或指定列有数据区域的最后一行行号

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **工作表** ：获取末行号操作所属工作表。仅支持字符串变量和字符串
- **列号** ：获取末行号的所属列索引（例：1，即获取第一列的末行号）。当此项为空时，取整表数据区域最后一行行号。仅支持整型变量和整型

### 输出

- **末行号** ：将取到的末行号存储在此整型变量内。

## 操作样例

1. 拖入**打开/新建**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击**...**选择本地Excel文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入**获取末行号**组件至项目流程中，填写sheet名称，填写要获取的列号，新建变量"rowNum"类型为Int32，用来存放行号：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLastRow1.png)

4. 点击运行，运行成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLastRow2.png)