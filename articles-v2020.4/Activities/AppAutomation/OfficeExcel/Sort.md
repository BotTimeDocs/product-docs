# 排序

对某列进行排序，提供&quot;升序，降序&quot;两种排序模式。工作表内所有行数据随之改变

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


输入

- **工作表** ：执行排序的目标工作表。仅支持字符串变量和字符串
- **列号** ：对此列进行排序操作。填入列索引（例：1，即对第一列进行排序）。仅支持整型变量和整型
- **顺序** ：下拉框选择排序模式为升序或降序

可选项

- **开始行号** ：执行开始排序的行号。若为空则默认从第一行开始执行排序。仅支持整型变量和整型

## 操作样例

1. 新建一个Excel文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Sort1.png)

2. 拖拽**打开/新建**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击**...**选择本地Excel文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽**排序**到**打开/新建**组件中，填写sheet名称"sheet2"，填写需要排序的列1，填写开始的行1：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Sort2.png)

5. 运行成功后打开Excel查看第1列从第1行开始已经按照升序排列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Sort3.png)
