# 反序列化

此组件可以将JSON字符串反序列化为.NET对象

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **JSON字符串** ：输入欲被反序列化为JSON数据；仅支持字符串变量和字符串

### 输出

- **结果** ：输入被反序列化后的对象；仅支持变量

## 操作样例

1. 在左侧**组件**区域找到**反序列化**和**写入日志**，并将其拖入**编辑区域**，按图示顺序连接，导入**Newtonsoft.Json.Linq**命名空间：![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject1.png)

2. 创建2个变量，其中1个变量类型为**String**，并对其赋值为*json类型的字符串*，例如**`"{'名称':'云扩RPA','版本':1.0}"`**或者**`"{""名称"":""云扩RPA"",""版本"":1.0}"`**（全为英文引号，注意单双引号和引号数量）。另一个变量类型为**JObject**，如果变量类型列表没有，单击**浏览类型**，在弹出窗口搜索**JObject**，选中后单击确定：![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject2.png)

3. 在组件**反序列化**右侧属性设置，输入刚才创建的2个变量：![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject3.png)

4. 在第一个写入日志的右侧日志内容中输入变量**json字符串**，在第2个写入日志的右侧日志内容中输入**json对象.ToString()**，然后单击**运行**流程，可以看到，反序列化后的**json对象**：![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject4.png)

> 若想了解更多关于**json**的内容，请参考网上的**[json教程](https://www.runoob.com/json/json-tutorial.html)**
