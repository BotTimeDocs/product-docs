# 条件(If)

根据是否满足指定条件决定下一步的执行内容

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

输入

- **判断条件** ：Boolean类型的表达式

## 操作样例

1. 拖入**获取结构化数据**组件，并指定网页端（例：[某股票网站](http://stockpage.10jqka.com.cn/1A0001/#refCountId=stockpage_5c3e9aef_93)）table元素，设置输出变量：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/if-1.png)

2. 拖入**条件（if）**组件，设置判断条件 dt.Rows.Count == 10 (判断数据表是否有10行数据)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/if-2.png)

3. 双击**条件（if）** 组件，并拖入两个**写入日志**组件放置条件容器内，根据判断条件True与False分别写入不同的日志文本：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/if-3.png)

4. 点击运行流程并查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/if-4.png)