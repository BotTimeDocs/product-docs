# 刷新透视表

此组件可实现刷新指定透视表的数据

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **工作表** ：透视表所属工作表。仅支持字符串变量和字符串
- **透视表名** ：输入透视表名称。仅支持整型变量和整型

## 操作样例

1. 新建一个透视表 "销售统计", 详情见 [新建透视表](./CreatePivotTable.md)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **刷新透视表** 组件到 **打开/新建** 组件中，填写工作表名称 "sheet1"，填写透视表名称 "销售统计"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RefreshPivotTable1.png)

5. 修改 excel 中收入列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RefreshPivotTable2.png)

6. 运行成功后，透视表汇总项已经更新：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RefreshPivotTable3.png)
