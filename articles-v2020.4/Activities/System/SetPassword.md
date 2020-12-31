# 设置密码

对敏感信息进行保护输入，安全存储和调用输出。使用此组件时，编辑和执行需在同一机器且必须是同一用户（包括机器人）；如果流程文件在不同机器或用户下运行，则需重新编辑&quot;设置密码&quot;组件的输入

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **设置密码** ：敏感信息。仅支持字符串变量和字符串

### 输出

- **赋值到变量** ：将敏感信息存储到此变量。仅支持字符串变量和字符串

## 操作样例
1. 拖入**设置密码**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setPassword-1.png)

2. 双击进入组件内部，配置属性参数：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setPassword-2.png)

3. 拖入**写入日志**组件，可以输出用户设置的密码：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setPassword-3.png)

4. 运行流程，查看控制台的输出：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setPassword-4.png)