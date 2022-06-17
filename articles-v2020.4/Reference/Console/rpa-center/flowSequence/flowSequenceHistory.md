# 流程编排执行记录


## 概述

在流程编排详情页的“执行记录”选项页中，展现了流程编排任务列表，可对当前流程编排下的任务进行快速查看，支持取消任务、删除日志、查看日志等操作。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-exctuehistory1.png)

 > **说明：**
>
> 1，支持以一次流程编排任务的视角，完整删除所有step节点的执行记录，但不支持删除单个step节点的执行日志（可通过RPA中心下的”执行记录“汇总入口操作）。
> 2，支持以流程编排视角，取消某节点处于“等待中/运行中"执行的编排任务（如当前编排正在执行step2节点），但不支持取消从单个step节点视角取消任务（可通过RPA中心下的”执行记录“汇总入口操作）

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
    ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-exctuehistory-job-status.png)


**执行实例（runinstance）状态**：

- 运行中：若任务有可用的机器人资源，且正在执行流程，则任务状态处于“运行中”；
- 已暂停：若用户在控制台或机器人端对”运行中“的任务操作”暂停“，则任务状态处于“已暂停”；
- 已取消：
         一次流程任务的执行结果，如执行次序1。
         情况1:用户在控制台端或机器人端，对”运行中/等待中/已暂停“的任务操作“取消”后，则任务状态处于“已取消”；
         情况2:根据设置的冲突处理策略，当机器人忙碌时，系统自动取消后续下发到此机器人的任务，则任务状态处于“已取消”； 
- 成功：机器人的一次流程任务执行结果为”成功“，如执行次序1；
- 失败：机器人的一次流程任务执行结果为“失败”，如执行次序1；
    ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-exctuehistory-runinstance-status.png)

## 查看流程编排的执行记录

- **查看任务（job）列表**
在流程编排详情页中，点击某一流程编排的“任务（job）列表”，可查看当前流程编排下生成的任务（job）列表，主要包括对应的流程部署名称、机器人、时间、状态等信息。
- **查看任务（job）下执行实例（runinstance）**
点击某一任务下的“展开”图标，可展开对应的执行实例列表，默认展示 3 条，如果超过 3 条点击“展开更多”按钮可以展开全部。
主要包括具体的执行机器人、开始时间、结束时间、状态等。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-exctuehistory-job-runinstance.png)


## 查看执行日志详情

在执行记录页面中点击任务下某一具体执行实例的“日志”链接，可查看任务的具体日志
![runinstance](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-exctuehistory-runinstance2.png)
![runinstance](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528workflow-excute-history-info2.png)


## 取消任务


对于”等待中/运行中/已暂停“的任务，可以操作”取消“。

取消编排任务，包含2个入口:
1. 在流程编排下的”执行记录“页面，若编排里的阶段，有处于”等待中/运行中/已暂停“的任务，则可以通过编排的视角，取消所有的step节点任务。
例如：编排里有4个step节点，当前step2处于”运行中“，则点击”取消后“，则step2、step3、step4节点的流程部署任务变为”已取消“。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-exctuehistory-cancel.png)

2. 在RPA中心下的”执行记录“汇总页面，可以对编排里任意一个处于”等待中/运行中/已暂停“的节点任务操作"取消"。若当前节点操作”取消“，则后续节点也变为”已取消“。
例如：编排里有4个step节点，当前step2处于”运行中“，则点击”取消后“，则step2、step3、step4节点的流程部署任务变为”已取消“。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-exctuehistory-cancel2.png)





## 调整任务优先级

对于”等待中“的任务，支持调整优先级。
调度队列中的任务将会按照任务优先级进行执行（0-5000）, 优先级越高则任务将会优先执行。
若您希望某一任务可以插队执行，则点击该任务的“调整优先级”选项，以调整优先级。
> **说明：**
>
> 调整编排任务的优先级，仅可在在RPA中心下的”执行记录“汇总页面操作，流程编排视角，不提供单个step节点任务的优先级调整入口。

![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-pri1.png)

你可以输入对应的优先级数字，数字越大则任务会被越优先执行。

![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-pri2.png)

