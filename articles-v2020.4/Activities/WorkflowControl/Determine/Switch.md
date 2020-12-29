# 条件(Switch)

指定C#表达式，并根据每个Case判断执行符合条件的流程

## 属性
###　基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

###　输入

- **表达式** ：输入C#表达式

## 操作样例

1. 拖入**输入框**组件，设置输出变量inputContent，并添加“标题”与“输入描述”，例：请输入任意数字。如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-1.png)

2. 拖入**条件（Swtich）** 组件，设置表达式 `Convert.ToInt32(inputContent) + 3 >= 10`:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-2.png)

3. 双击展开条件Switch组件，并点击 “Case True”模块，拖入**写入日志**组件至容器内，填入当表达式为真的描述：您输入的数字大于或等于7。用相同的操作设置“Case False”模块：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-3.png)

4. 保存并点击运行流程，查看日志显示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/switch-4.png)