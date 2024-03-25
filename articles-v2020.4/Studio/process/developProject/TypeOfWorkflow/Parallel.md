# 并行处理流程

## 概述

**并行处理流程**用于创建在同一机器人上与某个前台流程并行运行的流程。为此，并行处理流程绝不能包含需要用户交互的组件。

> **说明：**
>
>- 仅当 **流程项目** 中支持“并行处理流程”功能，**组件项目** 中暂不支持。
>- 仅当运行/调试整个流程时，才会调用“并行处理流程”。
>- 同一流程项目中，有且仅有一个该流程。
>- 主流程结束运行时，“并行处理流程”也将结束。

## 使用示例

1. 在编辑器中设计 **主流程** 和 **并行处理流程**。

    - **主流程（Main.xaml）**：打开“记事本”应用程序，并重复多次写入一段文本。

    ![主流程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/parallelmain20210916.png)

    - **并行处理流程(Parallel.xaml)**：当主流程中打开的记事本出现弹框时，则写入一段日志后关闭弹窗。

    ![并行处理流程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/parallel20210916.png)

2. 保存并运行流程。
3. 在流程运行时，点击“记事本”应用程序的“帮助 > 关于记事本”菜单。
4. 查看流程运行结果：“并行处理流程”辅助“主流程”执行了关闭弹窗的操作，同时主流程运行结束后，并行处理流程也随之结束。

    ![结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/result20210916.png)

> 需要在单个流程中并行任务的请参考组件：[并行](https://academy.encoo.com/wiki/Activities/WorkflowControl/Parallel.md)
