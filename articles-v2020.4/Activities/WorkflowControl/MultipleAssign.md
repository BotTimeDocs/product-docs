# 赋值(多个)

支持对最多10个变量进行赋值

## 属性
###　基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

## 操作样例
1. 拖入**赋值（多个）** 组件，创建变量 a 与 b，变量类型为Int32，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/multipleAssign-1.png)

2. 填入变量名至赋值组件并填入对应的值，拖入**确认框**组件，填入标题及描述`(a+b).ToString()`:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/multipleAssign-2.png)

3. 运行流程查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/multipleAssign-3.png)