# 任务计划管理
任务计划主要用于用户可自由配置各时间维度任务执行计划，调度机器人执行各类流程，从而实现对流程执行统一规划及调度。

## 任务计划列表查看
点击某一流程部署的“任务计划”按钮，即可切换查看该流程部署名下所有的任务计划。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow10.png)
## 新建任务计划

**第一步，填写任务计划详情配置**

1）基本信息：定时计划名称、流程部署名称、流程包名称 & 版本号。
![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow11.png)

2）计划时间(任务的定时执行时间)：
- 按分钟
- 按小时
- 按天
- 按周
- 按月
- 按cron表达式

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow12.png)

对于按照cron表达式执行定时计划任务，若了解cron表达式可自行根据规则编写，或通过云扩提供的cron表达式生成网站进行生成。

3）开始任务计划时间、停用任务计划时间
开始时间：到达开始时间之后，任务计划才会生效；
停用时间：到达停用时间之后，任务计划不会再生成任务。

**第二步，执行目标及参数确认**
1）队列名称/机器人名称：如果流程部署配置的执行方式为队列执行，此处展示队列名称及备注；若流程部署配置的执行方式为指定机器人，则展示具体机器人名称及状态。

2）参数信息：展示当前流程包中的参数值，若流程部署已对某参数值进行修改则此处将展示最新值。可在当前环节通过手动填写或导入资产进行重新赋值。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow13.png)
完成定时计划填写后，点击“保存”即可，定时计划将在设置的开始/停用时间自动启用或停用。

**备注：**
- 流程部署的执行目标为指定机器人时：每次任务计划触发时每个机器人均会执行一次该流程。即关联了N个机器人，每次任务计划触发时将会生成N个流程任务。
- 流程部署的执行目标为指定队列时：每次任务计划触发时该流程仅会执行一次，即生成一个流程任务在队列中动态分配。

## 查看及编辑任务计划详情
点击某一任务计划的“查看”按钮即可查看对应的任务计划详情。点击“编辑”按钮后即可开始对任务计划进行编辑，完成后点击“保存”按钮即可。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow14.png)

## 查看任务计划日志
点击某一任务计划的操作选项中的“查看日志”按钮即可查看该任务计划的启用、停用、创建任务情况，便于对任务计划进行跟踪。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow15.png)

## 启用/停用任务计划
你可以在任务计划列表中点击“操作”选项中的启用/停用按钮，对当前任务计划进行启用/停用操作。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow16.png)
