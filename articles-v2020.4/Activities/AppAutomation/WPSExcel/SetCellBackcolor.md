# 设置单元格背景色

对指定单元格进行填充背景色操作。提供拾色器辅助色号的填写，同时可填入&quot;获取单元格背景色&quot;的输出变量作为指定单元格的背景色

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **工作表** ：目标单元格所属工作表。仅支持字符串变量和字符串
- **单元格** ：填充颜色的目标单元格，可填入单元格地址或单元格区域。此处不可为空，否则运行失败
- **颜色** ：取此值作为填充色。可手动输入或使用拾色器辅助


## 操作样例
1. 新建一个Excel文件:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps20.png)

2. 拖入**打开/新建**组件，不勾选新建文件，再填入需要打开的Excel文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击**打开/新建**组件，拖入**设置单元格背景色**组件，填写工作表和单元格位置以及需要设置的颜色代码:
    - 举例：红色为#FF0000
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps21.png)


4. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps22.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps23.png)