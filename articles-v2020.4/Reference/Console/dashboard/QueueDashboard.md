# 机器人组监控

机器人组监控，用户可按今日、最近 7 天、最近 30 天或自定义时间段，从多维度对调度队列中机器人、流程任务运行调度情况进行统计监测。

![机器人组监控](https://docimages.blob.core.chinacloudapi.cn/images/Console/1219robotgroup-all.png)

### 机器人组任务分布

- **机器人组任务分布（饼状图）：** 在指定时间区间内，统计**机器人组**执行任务状态的数量分布，状态包含等待中、运行中、已暂停、已取消、成功、失败。统计任务状态。
- **执行任务总数：** 在指定时间区间内，**机器人组**执行任务的总数，任务总数以runinstance为计算单位（如一次job可能包含3次错误重试的runinstance）。
- **今日新增：** 今天内，**机器人组**执行任务的总数，任务总数以runinstance为计算单位（如一次job可能包含3次错误重试的runinstance）。

> **说明：**
>
> 1，机器人组一定属于当前部门，但机器人组里的绑定的机器人可以是本部门的，也可以是分享来的，皆视为在机器人组内。
>
> 2，默认统计当前部门，同时也支持[当前部门+包含子部门]的统计方式。
>
> 3，*详见名词解释*：[任务job与执行实例runinstance](./../../Glossary.md)

### 机器人组执行任务总时长

- **任务总时长TOP10（饼状图）**：机器人组作为执行目标，任务下发给机器人组，且以机器人组为统计单位。在指定时间区间内，[当前部门下机器人组里的所有机器人]执行任务时长较高的前10名机器人组。机器人组的执行任务时长=机器人组里所有机器人的任务[结束时间-开始时间]之和。
- **执行任务总时长**：机器人组作为执行目标，任务下发给机器人组，且以机器人组为统计单位。在指定时间区间内，[当前部门下机器人组的所有机器人]执行任务的总时长，时长以runinstance的执行时间为颗粒度计算（如一次job可能包含3次错误重试的runinstance），一次执行时间=结束时间-开始时间。
- **今日新增**：机器人组作为执行目标，任务下发给机器人组，且以机器人组为统计单位。在今天内，[当前部门下机器人组的所有机器人]执行任务的总时长，时长以runinstance的执行时间为颗粒度计算（如一次job可能包含3次错误重试的runinstance），一次执行时间=结束时间-开始时间。

> **说明：**
>
> 1，机器人组一定属于当前部门，但机器人组里的绑定的机器人可以是本部门的，也可以是分享来的，皆视为在机器人组内。
>
> 2，*详见名词解释*：[任务job与执行实例run instance](./../../Glossary.md)

### 机器人组忙碌比

- **平均忙碌比**：机器人组作为执行目标，任务下发给机器人组，且以机器人组为统计单位。在指定时间区间内，[当前部门下机器人组里的机器人]的实际运行时间总和比上机器人饱和运行时间总和。饱和运行，即机器人组里的所有机器人7*24小时无休运行。
- **今日忙碌比**：机器人组作为执行目标，任务下发给机器人组，且以机器人组为统计单位。在今天内，[当前部门下机器人组里的机器人]的实际运行时间总和比上机器人饱和运行时间总和。饱和运行，即机器人组里的所有机器人7*24小时无休运行。

> **说明：**
>
> 1，机器人组一定属于当前部门，但机器人组里的绑定的机器人可以是本部门的，也可以是分享来的，皆视为在机器人组内。

### 机器人组成功率TOP10

- **机器人组成功率TOP10**：成功，即任务执行成功。机器人组作为执行目标，任务下发给机器人组，且以机器人组为统计单位。在指定时间区间内，[当前部门下机器人组里的机器人]的任务执行成功率较高的前10名机器人组。

### 机器人组失败率TOP10

- **机器人组失败率TOP10**：失败，即任务执行失败。机器人组作为执行目标，任务下发给机器人组，且以机器人组为统计单位。在指定时间区间内，[当前部门下机器人组里的机器人]的任务执行失败率较高的前10名机器人组。
