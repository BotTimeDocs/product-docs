# 写入单元格

使用组件，写入数据到 Excel 文件中的指定单元格。

##  属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **数据** ：写入单元格内的数据。仅支持字符串变量和字符串。
    > 可传入&quot; 读取单元格&quot; 的输出变量，实现复制粘贴效果，同时保持复制源的数据格式。

### 目标

- **单元格** ：写入数据的目标单元格地址。可输入单元格或区域，仅支持字符串变量和字符串。当输入区域时，则在指定区域每一个单元格内输入相同数据。
- **工作表** ：写入数据的目标工作表。仅支持字符串变量和字符串。若指定工作表不存在，则在 Excel 文件中新建该工作表。

## 操作样例
1. 拖入 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

2. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

3. 拖入 **读取单元格** 组件至项目流程中，填写 sheet 名称，填写单元格名称，新建变量 "cellContent" 类型为 String，用来存放单元格内容：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCell1.png)

4. 拖入 **写入单元格** 组件至项目流程中，填写 sheet 名称，填写单元格名称，填写要写入的变量，这里使用 "cellContent"。也就是使用 A1 的内容写入 A2：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCell2.png)

5. 点击运行，运行成功后。打开 Excel 查看 A1 的内容已经写入 A2：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ReadCell3.png)