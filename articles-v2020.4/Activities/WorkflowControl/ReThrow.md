# 重新抛出异常

支持在流程执行时重新将异常的原始信息抛出

## 属性
###　基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称

## 操作样例
1. 拖入**循环操作（While）** 组件，设置变量，输入循环条件，并拖入**错误捕获（Try Catch）** 组件至容器内，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Rethrow-1.png)

2. 双击展开错误捕获（Try Catch）组件，并分别拖入**点击**与**赋值**组件，指定对应元素，设置变量递增：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Rethrow-2.png)

3. 拖入**重新抛出异常**组件至Catch容器内，然后保存并点击运行流程，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Rethrow-3.png)
