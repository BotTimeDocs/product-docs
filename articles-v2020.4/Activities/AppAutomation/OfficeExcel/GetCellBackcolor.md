# 获取单元格背景色

提取指定单元格的背景色，并返回十六进制值。同时可使用返回值作为&quot;设置单元格背景色&quot;的输入

## 属性

### 基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **工作表** ：指定目标单元格所属工作表名称。仅支持字符串变量和字符串
- **单元格** ：提取背景色的目标单元格，不支持单元格区域（填入区域时将无法执行）。仅支持字符串变量和字符串

### 输出

- **颜色** ：输出指定单元格背景色，例如"#FFFFFF"。仅支持字符串变量和字符串

## 操作样例

1. 拖入**打开/新建**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击**...**选择本地Excel文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入**获取单元格背景色**组件至项目流程中，填写sheet名称“sheet1”，填写单元格名称“A1”，新建变量"color"类型为String，属性面板颜色配置变量"color"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetCellBackColor1.png)

4. 点击运行，运行成功后打开excel，对应的单元格或者区域颜色设置成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetCellBackColor2.png)
