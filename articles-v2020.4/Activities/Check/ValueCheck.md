# 值校验

将两个值进行对比，根据对比条件返回布尔值

可使用此种方法取得元素的属性值：IUiObject.**GetProperty**(“attributeName”).toString()



## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **实际值** ：进行对比的值。仅支持字符串变量和字符串
- **期望值** ：进行对比的值。仅支持字符串变量和字符串
- **校验模式** ：对实际值和期望值进行对比的模式，例如等于，大于，小于等，可通过下拉框选择

    >**说明：**
    > 如下列出较难理解的校验符号。
    > - 开始于：确定字符串是否以指定字符串的字符开头，返回true或false。
    > - 结束于：确定字符串是否以指定字符串的字符结束，返回true或false。

### 输出

- **结果** ：输出两个值对比后的Boolean类型结果

## 操作样例
1. 拖入**值校验**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/valueCheck-1.png)

2. 以校验模式为“开始于”举个例子，设置期望值为“a”，实际值为"abc"，设置变量“flag”输出两个值对比后的Boolean类型结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/valueCheck-2.png)

3. 拖入**写入日志**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/valueCheck-3.png)

4. 运行流程，控制台输出两个值对比后的Boolean类型结果，如，“True”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/valueCheck-4.png)
