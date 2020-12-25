# 选择文件

指定筛选的文件类型，在运行时弹窗选择文件后输出

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

可选项

- **描述** ：指定选择文件弹窗的标题
- **文件筛选** ：指定欲过滤的文件类型；默认为所有文件，不过滤。可从下拉列表选择，也可手动输入

输出

- **选择的文件** ：输出选择的文件绝对路径；仅支持字符串变量和字符串

## 操作样例
1. 拖入**选择文件**组件，添加输出结果变量filePath：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFile-1.png)
2. 拖入**写入日志**组件，可以输出选择的文件路径信息
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFile-2.png)
3. 运行流程，**选择文件**组件开始运行，弹出选择文件的框
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFile-3.png)
4. 手动选择一个文件，查看输出的文件路径信息
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/selectFile-4.png)
