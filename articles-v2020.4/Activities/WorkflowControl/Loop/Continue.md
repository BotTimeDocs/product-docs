# 继续循环

跳出当前次循环，执行下一次循环

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

## 操作样例

1. 创建变量list，变量类型为`List<String>`, 默认值为 `new List<String>{"a","b","1","c"}`:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/continue-1.png)

2. 拖入**循环操作（For Each）** 组件，将变量list作为循环体：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/continue-2.png)

3. 拖入流程图组件至循环操作（For Each）容器内，拖入**流程决策**组件并输入判断条件 item == 1:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/continue-3.png)

4. 判断条件为真时跳出当次循环并开始执行下一次循环；判断条件为假时将当前值作为日志文本输出。拖入**继续循环**组件与**写入日志**组件，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/continue-4.png)

5. 点击运行流程并查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/continue-5.png)
