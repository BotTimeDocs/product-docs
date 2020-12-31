# 保存为CSV文件

将数据表保存为CSV文件

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **数据表** ：将此数据表保存为CSV文件
- **文件路径** ：保存的CSV文件路径。支持相对和绝对路径。需提供文件名且带后缀。例如：“E:\DT.csv”。无后缀则视为文件夹，即没有提供文件名，报错。如果有文件夹不存在，则新建。仅支持字符串变量和字符串

### 可选项

- **分隔符** ：指定CSV文件的分隔符。此属性可不填写，默认使用逗号。仅支持字符变量和字符
- **编码方式** ：文件的编码方式。可以在 [此处](../Appendix/Encoding.md) 找到每个字符编码的完整代码列表。要指定要使用的编码类型，请使用&quot; 名称&quot;字段中的值。如果未指定编码类型，则默认为UTF-8。仅支持字符串变量和字符串

## 操作样例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateRow20201228.png)

3. 拖入**保存为CSV文件**组件，输入数据表变量，例：table，创建类型为String的路径变量并给出默认值，例：filepath:"C:\云扩科技\savetable.csv"，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SaveToCSV20201229.png)

4. 点击运行，查看运行结果，检查路径是否保存CSV文件成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SaveToCSV2020122902.png)