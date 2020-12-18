# 遍历循环（For Each）

支持用户对某一对象内的数据逐个进行访问并处理

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

输入
- **循环体** ：被执行循环的对象集合

输出
- **当前索引** ：当前次循环的对象索引

## 操作样例
1. 设置变量list，变量类型为List\<String\>, 并添加默认值 new List\<String\>{"a","b","c"},如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/forEach-1.png)

2. 拖入**循环操作（For Each）** 组件，并设置循环体为变量list：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/forEach-2.png)

2. 双击展开组件，将**写入日志** 组件拖入循环操作（For Each）组件容器内，并设置日志文本为：“当前值是： ” + item，然后点击运行流程并查看输出日志内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/forEach-3.png)
