# 设置文字颜色

对指定单元格的内容设置颜色。此组件仅可在&quot; 打开/新建&quot; 组件中使用，默认取其工作簿，无需再次输入

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **工作表** ：指定目标单元格所属工作表名称。仅支持字符串变量和字符串
- **单元格** ：指定设置颜色的目标单元格，可填入单元格地址或单元格区域。此处不可为空，否则运行失败
- **颜色** ：指定颜色(16 进制颜色码)；支持手动输入和从拾色器选择；仅支持字符串变量和字符串

## 操作样例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetTextColor1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **设置文字颜色** 到 **打开/新建** 组件中，填写 sheet 名称 "sheet2"，填写单元格名称 "A1"，点击颜色选择框，选择颜色：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetTextColor2.png)

5. 点击颜色选择框，点击高级，拖动滑块或者直接填写编码选择需要的颜色：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetTextColor3.png)

6. 点击颜色输入框，直接输入颜色编码：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetTextColor4.png)

7. 运行成功后，打开 excel，看到 A1 的字体颜色变为红色：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SetTextColor5.png)