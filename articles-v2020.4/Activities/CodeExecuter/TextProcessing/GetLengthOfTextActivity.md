# 获取文本长度

获取文本的长度

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **文本** ：输入文本数据。仅支持字符串变量和字符串

### 输出
- **长度** ：输出当前文本的长度。仅支持Int变量
## 操作样例
1.拖入**获取文本长度**组件，创建相应变量并填入，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010501.png)

2.拖入其它组件，例：拖入**写入日志**组件，将获取到的文本长度以文本格式输出到日志中，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010502.png)

3.点击运行，流程运行成功，成功获取到文本的长度，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010503.png)