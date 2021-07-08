# 遍历行

遍历指定数据表中的每一行，同时可返回当前行索引

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **数据表** ：取此表执行遍历操作

### 输出

- **当前行索引** ：将当前正在被遍历的行索引存储在此变量。仅支持整型变量和整型

## 操作样例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RemoveDuplicateRow20201228.png)

3. 拖入**遍历行**组件，双击打开之后输入数据表变量，例：table，创建int32类型的变量用来存放当前索引值，例：currindex，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ForEachRow20201228.png)

4. 拖入**写入日志**组件和**赋值**组件，因为当前行索引从0开始，当前行的值是行索引加一，所以给currindex赋值变量每次加一，例：currindex=currindex+1，写入日志内容为每一行的姓名的值，例："当前为第"+currindex+"行，姓名为："+row["姓名"]，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ForEachRow2020122802.png)

5. 点击运行，查看运行结果，检查写入日志的每行的行值和姓名值：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ForEachRow202012280203.png)
