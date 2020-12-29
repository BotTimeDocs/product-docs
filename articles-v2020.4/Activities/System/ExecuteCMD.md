# 执行命令行

执行CMD命令行，并提供返回值。例如使用命令行实现60秒后定时关机： &quot;shutdown -s -t 60&quot;
注意：此组件也支持对Python文件的操作，例如：在“命令行”属性中填写“Python Test.py arg1 arg2”, 其中“arg1”和“arg2”为参数。

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


输入

- **工作目录** ：指定运行命令的工作目录
- **命令行** ：执行该命令行。仅支持字符串变量和字符串

输出

- **输出** ：将命令行执行后的结果存储到此变量
## 操作样例
1. 拖入**执行命令行**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-1.png)

2. 双击进入组件内部，设置参数：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-2.png)

3. 拖入**写入日志**组件，可以输出执行命令行的结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-3.png)

4. 运行流程，查看控制台的输出：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-4.png)
