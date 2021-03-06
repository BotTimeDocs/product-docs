# 获取页数

可实现获取指定 PDF 文件的总页数

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **文件路径** ：输入欲被获取页数的 PDF 文件路径。仅支持字符串变量和字符串

### 可选项

- **总页数** ：输出 PDF 文件的总页数

## 操作样例

1. 拖入 **获取页数** 组件至项目流程中，并设置变量 page_num(int32)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetPageNumbers_1.png)

2. 双击打开获取页数，选取 pdf，例："D:\\滴滴电子发票 (1).pdf"，选择需要的页数范围，输入生成路径，在输出中添加 page_num, 如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetPageNumbers_2.png)

3. 点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetPageNumbers_3.png)