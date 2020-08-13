# 状态

*状态*组件是状态机中使用的组件，是状态机工作流的基础组成部分。

*状态*组件必须放置在*状态机组件中*。

*状态*组件包括三个可编辑区域：
- Entry 区域：包含在 Entry 区域的组件会在工作流进入该*状态*组件时被执行；
- Exit 区域：包含在 Exit 区域的组件会在工作流离开该*状态*组件时被执行；
- Transition 区域：通过设定 Transition 中的内容，你可以实现多个状态之间的转换。

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。

## 示例
你可以参考 [*GuessNumber*](https://docimages.blob.core.chinacloudapi.cn/images/dgsSample/GuessNumber.dgs) 流程，了解状态机相关组件的具体用法。

