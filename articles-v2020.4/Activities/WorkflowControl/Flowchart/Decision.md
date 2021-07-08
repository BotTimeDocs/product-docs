# 流程决策

根据是否满足指定条件，选择执行流程图中两个分支。此组件只能在流程图中使用，效果类似&quot;条件&quot;组件

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称

### 输入

- **决策条件** ：Boolean类型的表达式

### 杂项

- **False 标签** ：决策为False，可自定义决策名称
- **True 标签** ：决策为True，可自定义决策名称

## 操作样例

1. 拖入**等待元素出现**组件，并指定元素、添加输出结果变量isTrue：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decision-1.png)

2. 拖入**流程决策**组件，将上步操作中的输出变量isTrue作为输入条件Condition：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decision-3.png)

3. 拖入两个**写入日志**组件，分别连接到决策组件True与False端，并添加元素是否出现的提示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decision-2.png)

4. 步骤1中指定元素的网页保持打开状态，运行流程并查看输出窗口中提示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/decision-4.png)
