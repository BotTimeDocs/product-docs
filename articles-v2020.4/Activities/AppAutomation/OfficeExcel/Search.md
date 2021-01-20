# 查找

在特定单元格区域内查找给定值，并返回第一个查找到的单元格地址。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入


## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **工作表** ：执行查找操作的目标工作表。仅支持字符串变量和字符串
- **区域** ：查找操作的目标单元格区域。为空时，默认查找全表
- **查找内容** ：取此值进行查找。仅支持字符串变量和字符串

### 输出

- **单元格地址** ：将查找到的第一个单元格地址存储在此变量。仅支持字符串变量和字符串

## 操作样例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Search1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **排序** 和 **写入日志** 到 **打开/新建** 组件中，填写 sheet 名称 "sheet2"，填写搜索区域，填写搜索的关键字“100”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Search2.png)

5. 运行成功后，输出面板打印关键字所在的位置：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Search3.png)