# 最终状态
*最终状态*组件是状态机中使用的组件，是状态机工作流的基础组成部分。状态机工作流中必须包含一个*最终状态*组件。

*最终状态*组件必须放置在*状态机组件中*。

*最终状态*组件包括一个可编辑区域：
- Entry 区域：包含在 Entry 区域的组件会在工作流进入该*最终状态*组件时被执行。

## 属性

###　基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。


## 操作样例

1. (实例说明：登录钉钉) 拖入**状态机**组件，并双击展开状态机：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-1.png)

2. 双击展开默认的**状态**组件，拖入**等待元素出现**组件至Entry容器内，指定钉钉登录后的任何一个元素，并设置输出结果变量，选择失败后继续为“是”，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-2.png)

3. 拖入**最终状态**组件，设置判断条件`isTrue == true`，双击展开最终状态并在Enter容器内拖入**确认框**组件，添加提示“钉钉登录成功”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-3.png)

4. 拖入**状态**组件，设置判断条件`isTrue == false`：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-5.png)

5. 双击展开组件，在Enter容器中编写好输入用户名、输入密码、点击登录及等待登录状态下界面元素流程，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-6.png)

6. 如果在第5步操作中等待元素，那么最终状态为已登录，流程设置如下：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-7.png)

你还可以参考 [*GuessNumber*](https://docimages.blob.core.chinacloudapi.cn/images/dgsSample/GuessNumber.dgs) 流程，了解状态机相关组件的具体用法。
