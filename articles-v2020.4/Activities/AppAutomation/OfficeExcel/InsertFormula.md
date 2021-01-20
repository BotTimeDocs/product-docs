# 插入公式

向单元格插入公式，并填充公式运行后的结果

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **工作表** ：插入公式的目标单元格所属工作表。仅支持字符串变量和字符串
- **单元格** ：执行插入公式操作的目标单元格，即接收执行公式的结果，支持区域。仅支持字符串变量和字符串
- **公式** ：插入的公式。支持两种写法：含公式名（例：SUM(A1, A2)），不含公式名（A1+A2）；两种写法均可省略等号。仅支持字符串变量和字符串

### 输出

- **执行结果** ：将公式执行结果存储在此变量

## 操作样例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InertFormula1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **插入公式组件** 到 **打开/新建** 组件中，填写工作表名称，单元格名称和公式：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InertFormula2.png)

5. 运行成功后，sheet1 的 A2 中插入公式“SUM(A1: D1)”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InertFormula3.png)