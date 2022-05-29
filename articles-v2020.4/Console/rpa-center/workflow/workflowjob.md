# 流程部署执行记录

## 概述

在流程部署详情页的“执行记录”选项页中，展现了流程部署任务列表，可对当前流程部署下的任务进行快速查看，支持查看任务详情、调整优先级、启用/停用任务、查看日志等操作。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-excute-history.png)


### 状态说明
*详见名词解释*：[任务job与执行实例runinstance](./../../../Glossary.md)
**任务（job）状态**：

- 等待：若任务没有可用的机器人资源，则任务状态处于”等待中“；
- 运行中：
         情况1：若任务有可用的机器人资源，且正在执行流程，则任务状态处于“运行中”；
         情况2：若任务还有重试机会(如执行次序2或3)，但是此时机器人被占用，正在等待机器人时，则任务状态处于”运行中“；
- 已暂停：若用户在控制台或机器人端对”运行中“的任务操作”暂停“，则任务状态处于“已暂停”；
- 已取消： 
         一次流程任务的最终状态。
         情况1:用户在控制台端或机器人端，对”运行中/等待中/已暂停“的任务操作“取消”后，则任务状态处于“已取消”；
         情况2:根据设置的冲突处理策略，当机器人忙碌时，系统自动取消后续下发到此机器人的任务，则任务状态处于“已取消”；
- 成功：
          一次流程任务的最终状态。
          一次任务，可能包含多次重试执行（如执行次序1、2、3），任务的最终状态基于最后一次重试执行结果。
- 失败：
         一次流程任务的最终状态。
         一次任务，可能包含多次重试执行（如执行次序1、2、3），任务的最终状态基于最后一次重试执行结果。
    ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-job-status.png)


**执行实例（runinstance）状态**：

- 运行中：若任务有可用的机器人资源，且正在执行流程，则任务状态处于“运行中”；
- 已暂停：若用户在控制台或机器人端对”运行中“的任务操作”暂停“，则任务状态处于“已暂停”；
- 已取消：
         一次流程任务的执行结果，如执行次序1。
         情况1:用户在控制台端或机器人端，对”运行中/等待中/已暂停“的任务操作“取消”后，则任务状态处于“已取消”；
         情况2:根据设置的冲突处理策略，当机器人忙碌时，系统自动取消后续下发到此机器人的任务，则任务状态处于“已取消”； 
- 成功：机器人的一次流程任务执行结果为”成功“，如执行次序1；
- 失败：机器人的一次流程任务执行结果为“失败”，如执行次序1；
    ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-runinstance-status.png)

## 查看流程部署任务

- **查看任务列表**
在流程部署详情页中，点击某一流程部署中的“任务列表”选项页，可查看当前流程部署下通过任意方式生成的任务列表，主要包括对应的流程部署名称、流程包名称、流程包版本、任务来源等信息。
- **查看任务（job）下执行实例（runinstance）**
点击某一任务下的“展开”图标，可展开对应的执行实例列表，默认展示 3 条，如果超过 3 条点击“展开更多”按钮可以展开全部。主要包括具体的执行机器人、开始时间、结束时间、状态等。


## 查看任务详情

点击某一任务操作栏中的“查看详情”选项，即可查看该任务的执行详情，任务详情主要包括执行基本信息、参数信息等内容。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-excute-history-info1.png)

## 查看日志详情

你可以通过如下方式，查看任务在机器人上的执行日志：

- **方式一**：在任务列表页面中点击任务下某一具体执行实例的“日志”链接，可查看任务在该机器人上执行的具体日志。

    ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-excute-history-info4.png)

- **方式二**：在“任务详情”页面，点击“查看日志”按钮，查看任务在该机器人上执行的具体日志。

    > **说明：**
    >
    > 日志主要包含日志时间、日志类型、日志级别、日志内容、日志截图等内容。可以在左上角的“日志”，可以切换并查看其他执行次序的执行情况。

    ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-excute-history-info2.png)

## 取消任务

对于”等待中/运行中/已暂停“的任务，可以操作”取消“。

![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-excute-history-cancel.png)



## 调整任务优先级

对于”等待中“的任务，支持调整优先级。
调度队列中的任务将会按照任务优先级进行执行（0-5000）, 优先级越高则任务将会优先执行。
若您希望某一任务可以插队执行，则点击该任务的“调整优先级”选项，以调整优先级。

![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-excute-history-pri.png)

你可以输入对应的优先级数字，数字越大则任务会被越优先执行。

![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-excute-history-pri2.png)
