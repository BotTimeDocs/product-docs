# 赋值

对指定变量进行赋值

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

输入
- **变量名** ：被赋值的变量名
- **值** ：赋值内容，需与被赋值的变量名类型相同

## 操作样例
1. 拖入**循环操作（Do While）** 组件，创建变量count，设置数据类型为Int32，默认值为1，并添加循环条件 count <= 3，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dowhile-1.png)

2. 双击展开组件，将**赋值**组件拖入循环操作（Do While）容器内，设置count递增，即 count = count + 1：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dowhile-2.png)

3. 拖入**写入日志**组件，填入打印内容: "循环次数： " + count.ToString()，并点击运行流程查看输出日志：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dowhile-3.png)