# 终止循环

跳出当前整个循环，执行循环后的组件

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

## 操作样例
1. 拖入**循环操作（While）** 组件，创建int32类型变量count，设置默认值为1，并添加循环条件 count <= 100:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/While-1.png)

2. 双击展开组件，拖入流程图组件至容器内并双击展开，拖入**流程决策** 组件，设置String类型变量t1，输入时间默认值，如："2020-12-18 16:35:00":
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/break-0.png)

3. 输入判断条件 System.DateTime.Now.CompareTo(Convert.ToDateTime(t1)) < 0 （获取当前时间并与指定时间t1做比较），如果值为真（即当前时间早于指定时间），则用**终止循环**组件来结束循环，如果值为假，用**赋值**组件递增循环变量count：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/break-2.png)

4. 点击运行流程，查看流程运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/break-1.png)