# 筛选

设置&quot; 筛选向导&quot; 中的条件，并依此对工作表进行条件筛选，同时将符合筛选条件的结果应用到工作表内

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **工作表** ：执行筛选的目标工作表。仅支持字符串变量和字符串
- **列号** ：执行筛选的目标列。仅支持整型变量和整型

## 操作样例

1. 新建一个 Excel 文件，在 A1: B8 处填入需要被读取的值:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps29.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **筛选** 组件至 **打开/新建** 组件中:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps30.png)

4. 双击 "筛选向导" 按钮，并配置筛选条件:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps31.png)

5. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps32.png)
