# 替换文本

支持将文本内容中符合条件的第一个内容替换为期望值

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **源文本** ：欲被替换的源文本数据。仅支持字符串变量和字符串
- **查找内容** ：指定欲被替换的内容。仅支持字符串变量和字符串
- **新内容** ：指定欲替换成的内容。仅支持字符串变量和字符串

### 输出

- **替换结果** ：替换后的结果。仅支持字符串变量

## 使用示例

1. 拖入**替换文本**组件至项目流程中

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReplaceTextActivity2021010501.png)

2. 创建变量，并将其填入对应输入框中，如下图所示：

![Image Text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReplaceTextActivity2021010502.png)

3. 拖入其它组件至流程中，例：拖入写入日志组件，如下图所示：

![Image Text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReplaceTextActivity2021010503.png)

4. 点击运行，流程运行成功，如下图：

![Image Text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReplaceTextActivity2021010504.png)