# 设置日志级别

控制日志输出的内容。此组件后的日志将按照所选级别输出。编辑器默认日志输出级别为Info，设置此组件&quot;日志级别&quot;属性为Debug后，可以查看更加详细的日志信息

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 日志

- **日志级别** ：共有三个选项：Debug,  Info, Error。选择Debug后，可查看最详细的日志信息；选择Info后，可查看Info和Error等级的日志信息；选择Error后，将只输出Error日志

## 操作样例
1. 拖入**设置日志级别**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-1.png)


2. 拖入3个**写入日志**组件到设计面板，日志级别分别选择“Debug”，“Info”，“Error”，并分别命名为“Debug日志”，“Info日志”，“Error日志”，下图展示的是设置的Debug日志：
- 设置Debug日志输出的日志信息为："我是一个Debug的日志"；
- 设置Info日志输出的日志信息为："我是一个Info的日志"；
- 设置日志输出的日志信息为："我是一个Error的日志"；

![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-2.png)


3. 选择**设置日志级别**组件的日志级别为“Debug”，运行流程，控制台输出Debug，Info，Error等级的日志信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-3.png)


4. 选择**设置日志级别**组件的日志级别为“Info”，运行流程，控制台输出Info, Error等级的日志信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-4.png)

5. 选择**设置日志级别**组件的日志级别为“Error”，运行流程，控制台只输出Error等级的日志信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setLoglevel-5.png)
