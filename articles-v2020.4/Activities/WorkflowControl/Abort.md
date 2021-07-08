# 终止流程

当执行到此组件时立即结束当前流程，不再执行后续流程。

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件。
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件。

## 操作样例

1. 拖入**循环操作（While）** 组件，创建变量count并设置循环条件 count <= 100：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-1.png)

2. 设置两个变量，分别为workEndDT & workStartDT，设置变量类型TimeSpan，默认值分别为`DateTime.Parse("7:30").TimeOfDay` & `DateTime.Parse("20:30").TimeOfDay`; 拖入**流程决策**组件，设置判断条件: `DateTime.Now.TimeOfDay > workEndDT && DateTime.Now.TimeOfDay < workStartDT`:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-2.png)

3. 如果判断条件为真，则用**终止流程**组件终止流程；如果判断条件为假，则用**赋值**组件进行变量递增，循环继续：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-3.png)

4. 点击运行流程，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-4.png)