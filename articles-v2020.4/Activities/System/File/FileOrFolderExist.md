# 文件/文件夹是否存在

判断指定文件或文件夹是否存在，并返回结果

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件。

### 输入

- **路径类型** ：下拉框选择判断类型为文件或文件夹
- **路径** ：执行判断的文件或文件夹路径。支持相对和绝对路径。仅支持字符串变量和字符串

### 输出

- **路径是否存在** ：将判断结果存储在此变量

## 操作样例

1. 拖入**文件/文件夹是否存在**组件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-1.png)

2. 双击进入组件内部，"路径"需手动输入，支持相对和绝对路径：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-2.png)

3. 新建变量"exists"，用于判断路径是否存在：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-3.png)

4. 搜索**写入日志**组件，并拖入组件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-4.png)

5. 运行流程，判断文件"E:\shirley\hello.txt"存在，输出"True"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-5.png)