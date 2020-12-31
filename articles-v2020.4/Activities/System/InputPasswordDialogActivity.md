# 输入密码

提供人机交互界面，弹框形式展现并且带有密码输入框，接收用户输入的密码值并可以输出输入的密码

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **标题** ：输入弹窗的标题。仅支持字符串变量和字符串
- **描述** ：输入弹窗中的描述信息，帮助用户进行输入密码的操作。仅支持字符串变量和字符串

### 输出

- **输入的密码** ：将输入的密码存储在此变量。仅支持字符串变量和字符串

## 操作样例
1. 拖入**输入密码**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-1.png)

2. 双击**输入密码**组件的空白处，配置属性参数：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-2.png)

3. 拖入**写入日志**组件到设计面板中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-3.png)

4. 保存并运行流程，输入密码“123456”，可以看到控制台打印出用户输入的密码值：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-4.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/inputPassword-5.png)