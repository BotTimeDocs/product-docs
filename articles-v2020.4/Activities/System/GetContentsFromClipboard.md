# 获取剪贴板文本

获取剪贴板的文本内容并以String类型输出

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输出

- **文本** ：输出String类型的剪贴板文本内容

## 操作样例

1. 拖入**获取剪贴板文本**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-1.png)

2. 双击进入组件内部，输出文本框填入变量“copy_text”，输出文本框输出String类型的剪贴板文本内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-2.png)

3. 拖入**写入日志**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-3.png)

4. 打开网页，复制一段内容到剪贴板上：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-4.png)

5. 运行流程，控制台输出获取的剪贴板上的文本内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-5.png)
