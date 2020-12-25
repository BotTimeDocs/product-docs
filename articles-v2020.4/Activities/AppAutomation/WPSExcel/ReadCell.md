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
- **单元格** ：目标单元格。仅支持字符串变量和字符串

输出

- **数据** ：输出读取的目标单元格内数据


## 操作样例
1. 新建一个Excel文件，在A1处填入需要被读取的值:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps4.png)

2. 拖入**打开/新建**组件，不勾选新建文件，再填入需要打开的Excel文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击**打开/新建**组件，拖入**读取单元格**组件至**打开/新建**组件中，填写工作表和单元格位置，在输出数据中写入变量来接收读取的内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps6.png)

4. 拖入**写入日志**组件，来显示读取单元格的内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps7.png)

5. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps8.png)