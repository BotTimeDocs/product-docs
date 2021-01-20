# 获取所有工作表名

获取工作簿内所有工作表名称。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输出

- **工作表名称** ：工作簿内所有工作表名存储到此变量。可结合循环组件输出或使用工作表名

## 操作样例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **获取所有工作表名** 组件到 **打开/新建** 组件中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AutoFillRange1.png)

5. 拖拽 **循环操作（For Each）** 到 **打开/新建** 组件中，拖拽 **写入日志** 到 **循环操作（For Each）** 组件中，填入变量：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName2.png)

6. 运行成功后，日志打印所有 sheet 名称：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetWorksheetsName3.png)
