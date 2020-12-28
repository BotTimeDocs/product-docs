# 状态机

你可以使用状态机相关组件实现基于状态机范例的工作流程。

在云扩的组件体系中，状态机组件是*状态*组件，*最终状态*组件和编制状态机工作流所需的其他组件的容器。在使用这些组件实现流程时，你必须将其放置在状态机组件中。

状态机是微软 .NET 框架中的一种编程范式，通过状态的改变实现程序逻辑的推进。关于状态机的详细信息，参看[状态机工作流](https://docs.microsoft.com/zh-cn/dotnet/framework/windows-workflow-foundation/state-machine-workflows)。

## 属性

### 基本

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

你还可以参考 [*GuessNumber*](https://docimages.blob.core.chinacloudapi.cn/images/dgsSample/GuessNumber.dgs) 流程，了解状态机相关组件的其他用法。

