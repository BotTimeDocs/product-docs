# 下拉选择框

提供人机交互界面，弹框形式展现并且带有下拉选择框，在界面选择动态填充的值并输出

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


输入

- **标题** ：下拉选择框的标题。仅支持字符串变量和字符串
- **下拉选项** ：动态填充的下拉选项。仅支持String[]变量和String数组

可选项

- **默认索引** ：下拉选项的默认索引值。仅支持Int变量和数值

输出

- **选中项** ：将选择的项存储在此变量。仅支持字符串变量和字符串
## 操作样例
1. 拖入**获取文件/文件夹列表**组件到设计面板，双击进入组件内部，设置参数。设置获取的文件路径，如"E:\shirley"，设置列表输出变量，如"files"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-1.png)

2. 拖入**下拉选择框**组件到设计面板，双击进入组件内部。
- 设置下拉选择框的标题，如"E盘shirley目录下的文件"；
- 下拉选项值为获取文件/文件夹列表组件输出的文件列表"files"；
- 设置变量“value”为输出的选中项：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-2.png)

3. 拖入**写入日志**组件，可以输出用户选择的下拉框的值：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-3.png)

4. 运行流程，选择下拉框的值“E:\shirley\hello.txt”，并点击“确认”按钮：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-4.png)

5. 查看控制台的输出，输出下拉框选择的值，E:\shirley\hello.txt：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dropDown-5.png)


