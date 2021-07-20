# 数据格式化

支持输入DateTime、Int等类型数据并转换成符合实际业务需要的数据格式（数值、百分比、货币和日期时间）

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **数据** ：被格式化的原数据；支持 Int、Int32、Int64、Float、Double、DateTime等数据类型

### 输出

- **格式化数据** ：将格式化后返回的值存储在此变量；支持String数据类型

## 使用示例

1. 拖入**数据格式化**组件，并创建1个**String**类型的变量，在右侧**输入**栏写入1个带有小数点的多位小数：
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData1.png)

2. 双击打开**数据格式化**组件，单击**设置格式**，格式类型选择**数值**，填写需要保留几位小数，**千位分隔符**可选可不选：
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData2.png)

3. 拖入1个**写入日志**组件，打印查看**数据格式化**后的变量：
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData3.png)

4. 单击运行，可以看到，**数据格式化**处理过后的变量结果，只保留了第2步中我们设置的2位小数。
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData4.png)

5. 选择其他格式类型，再次**运行**流程，输出结果会成为相应的格式：
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData5.png)
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData6.png)
