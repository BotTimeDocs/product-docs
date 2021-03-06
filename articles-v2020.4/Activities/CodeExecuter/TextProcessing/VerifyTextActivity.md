# 验证文本有效性

使用正则表达式对整段源文本内容验证是否匹配期望值

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入


- **源文本** ：欲被验证的源文本数据。仅支持字符串变量和字符串
- **验证规则** ：点击“设置验证规则”后在弹窗中指定验证的规则

### 输出

- **验证结果** ：验证的结果。仅支持Boolean变量

## 操作样例

1. 拖入**验证文本有效性**组件至项目流程中

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010401.png)

2. 选中组件，点击展开提取规则。以邮箱地址为例，点击邮箱地址点击确定。创建变量，String类型变量及Boolean类型变量，并输入至源文本及验证结果中。如下图所示：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010402.png)

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010403.png)

3. 拖入写入日志组件将验证结果以字符串格式输出。点击运行，查看运行结果，验证文本结果为成功。如下图所示：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010404.png)

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010405.png)