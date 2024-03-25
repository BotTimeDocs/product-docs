# 管理执行记录

## 查看任务执行记录列表

进入“任务记录 " 页面，可以查看所有流程部署通过任何启动方式所触发的流程任务的执行状况。

## 搜索任务记录

支持通过关键字（流程部署、流程包）、状态、[来源场景、启动方式](./aboutJob.md)、时间，来筛选记录。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console13.png)

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
  ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console14.png)

**执行实例（runinstance）状态**：

- 运行中：若任务有可用的机器人资源，且正在执行流程，则任务状态处于“运行中”；
- 已暂停：若用户在控制台或机器人端对”运行中“的任务操作”暂停“，则任务状态处于“已暂停”；
- 已取消：
  一次流程任务的执行结果，如执行次序1。
  情况1:用户在控制台端或机器人端，对”运行中/等待中/已暂停“的任务操作“取消”后，则任务状态处于“已取消”；
  情况2:根据设置的冲突处理策略，当机器人忙碌时，系统自动取消后续下发到此机器人的任务，则任务状态处于“已取消”；
- 成功：机器人的一次流程任务执行结果为”成功“，如执行次序1；
- 失败：机器人的一次流程任务执行结果为“失败”，如执行次序1；
  ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console15.png)

### 查看任务下的执行实例

单击某一任务下的“展开”图标，可展开对应的执行实例列表，默认展示 3 条，如果超过 3 条，点击“展开更多”按钮可以展开全部。主要包括具体的执行机器人、开始时间、结束时间、状态等。

![查看任务下的执行实例](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console16.png)

### 查看实例的日志详情

**日志详情查看入口**

1. 在任务列表页面中，点击任务下某一具体执行实例的“日志”按钮，即可查看任务在该机器人上执行的具体日志。

   ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console16.png)
2. 也可在“任务详情”页面中点击“查看日志”按钮查看任务在该机器人上执行的具体日志。

   ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528history-info2.png)

**日志详情页面操作**
  支持查看、过滤10万条以内的日志数据；超出部分，需下载查看。
  ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console20.png)

> **说明：**
>
> 日志详情页面，主要包含日志时间、日志类型、日志级别、日志内容、日志截图等内容。可以在左上角的“日志切换”中快速切换该任务在其他机器人上的执行日志。

## 查看任务基本信息

单击某一job任务后的“查看”按钮即可查看该任务的执行详情，任务详情主要包括执行基本信息、参数信息等内容。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console17.png)

## 调整任务优先级

对于”等待种“的任务，支持调整任务优先级。
调度队列中的任务将会按照任务优先级进行执行（0-5000）, 优先级越高则任务将会被优先执行。
若您希望某一任务可以插队执行，则点击该任务的“调整优先级”按钮以调整优先级。

  ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3editpriority1.png)

你可以输入对应的优先级数字，数字越大则任务会被越优先执行。

  ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3editpriority2.png)

## 取消任务

可以对等待中/运行中/已暂停的任务，操作取消。

![取消任务](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console18.png)

- 若该任务取消时属于未指派给机器人状态，则直接取消。
- 若该任务终止时已经指派给某一机器人正在执行，则向机器人发送指令进行取消，当前任务会执行失败。

## 批量操作

任务记录页面中的任务支持批量操作功能，勾选页面任务列表左侧的筛选框后，单击页面右上方的“批量操作”按钮，可进行批量调整优先级、批量执行、批量取消执行操作。

  ![批量操作](https://docimages.blob.core.chinacloudapi.cn/images/Console/0626-console19.png)

