# 抛出异常

支持在流程执行时主动抛出异常

## 属性
###　基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称

###　输入
- **异常** ：设置需要抛出的异常类型及信息

## 操作样例
1. 拖入**等待元素出现**组件并指定元素，设置失败后继续为“是”，添加输出结果变量isTrue :
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Throw-1.png)

2. 拖入**流程决策**组件，输入条件isTrue:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Throw-2.png)

3. 拖入**抛出异常**组件，输入异常信息内容 `new Exception("未找到元素")`：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Throw-3.png)

4. 保存并点击运行流程，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Throw-4.png)