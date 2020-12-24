# 状态机

你可以使用状态机相关组件实现基于状态机范例的工作流程。

在云扩的组件体系中，状态机组件是*状态*组件，*最终状态*组件和编制状态机工作流所需的其他组件的容器。在使用这些组件实现流程时，你必须将其放置在状态机组件中。

状态机是微软 .NET 框架中的一种编程范式，通过状态的改变实现程序逻辑的推进。关于状态机的详细信息，参看[状态机工作流](https://docs.microsoft.com/zh-cn/dotnet/framework/windows-workflow-foundation/state-machine-workflows)。

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。

## 示例
你可以参考 [*GuessNumber*](https://docimages.blob.core.chinacloudapi.cn/images/dgsSample/GuessNumber.dgs) 流程，了解状态机相关组件的具体用法。

