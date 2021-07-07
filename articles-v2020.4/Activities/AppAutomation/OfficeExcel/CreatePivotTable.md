# 创建透视表

此组件可实现在 Excel 中创建透视表

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 目标位置

- **目标工作表** ：输入创建的透视表所在目标工作表。仅支持字符串变量和字符串
- **目标区域** ：输入创建的透视表所在目标区域。仅支持字符串变量和字符串
- **透视表名称** ：输入创建的透视表名称。仅支持字符串变量和字符串

  > **说明：**
  >
  > 在“创建透视表”弹窗中，需指定透视表字段，需输入字母列号，例如：在“筛选”中输入“A, B”，则创建的透视表以 A 列和 B 列作为筛选列。

### 数据源

- **源表名** ：输入数据源中的表名（和“源区域”属性互斥，二选一）。仅支持字符串变量和字符串
- **源工作表** ：输入数据源所属工作表。仅支持字符串变量和字符串
- **源区域** ：输入数据源中的区域（和“源表名”属性互斥，二选一）。仅支持字符串变量和字符串

## 操作样例

1. 新建一个 Excel 文件，如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable1.png)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **创建透视表** 组件到 **打开/新建** 组件中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable2.png)

5. 点击创建透视表向导，填写源工作表“sheet1”，区域 "A1: D11"；填写目标工作表“sheet1”，目标区域 "F1: H11"，透视表名称 "销售统计"；填写透视表字段如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable3.png)

6. 运行成功后，在目标区域生成如下透视表：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/CreatePivotTable4.png)
