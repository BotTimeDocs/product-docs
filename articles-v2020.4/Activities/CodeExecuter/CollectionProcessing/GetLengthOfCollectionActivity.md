# 获取集合长度

获取指定集合的长度

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **集合** ：指定目标集合

### 输出

- **长度** ：输出目标集合的长度；仅可接Int变量

## 操作样例

1. 拖入**初始化集合**组件，设置变量`集合List`，变量类型为`List<String>`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InitializeCollectionActivity1.png)
2. 拖入**添加对象**组件，**输入**需要添加的对象`"A1"`，**输入/输出**`集合List`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddToCollectionActivity1.png)
3. 拖入**获取集合长度**组件，新建变量`集合count`，**输入**变量`集合List`，**输出**长度变量`集合count`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfCollectionActivity1.png)
4. 拖入**写入日志**组件，打印`集合List`的长度，输入**日志内容**`集合count.ToString()`，打印结果为`1`：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfCollectionActivity2.png)
