# 提取文本

支持提取指定文本内容中符合条件（正则表达式）的第一个结果，源文本内容不变

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **提取规则** ：点击“设置提取规则”后在弹窗中指定提取的规则
- **源文本** ：欲被提取的源文本数据。仅支持字符串变量和字符串

### 输出

- **提取结果** ：执行文本提取规则后提取的数据结果。仅支持字符串变量

## 操作样例
1. 拖入**提取文本**组件至项目流程中

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010401.png)

2. 创建变量，并输入至源文本及验证结果中。选中**提取文本**组件，点击展开提取规则。以手机号码地址为例：点击电话号码，点击手机号码，点击确定。如下图所示

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010402.png)

3. 拖入其它组件至流程中，例：**写入日志**组件，输入日志内容为运行结果（result）

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010403.png)

4. 点击运行，查看运行结果。成功将源文本中手机号提取出来，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExtractTextActivity2021010404.png)

