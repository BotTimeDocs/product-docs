# 管理定时任务

**定时任务**，用户通过配置定时计划、时区等，让业务流程按照既定的时间策略调度运行。

## 查看定时任务列表

在流程部署详情页中，单击任一流程部署的“定时任务”选项页，即可切换查看该流程部署名下所有的定时任务。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/workflowTriggerList.png)

## 新建定时任务
### 第一步，单击“+新建”
在流程部署详情页的“定时任务”选项页中，单击“+新建” ，在弹出的新建对话框中，填写定时任务详情配置。新建页面包含3个部分：基础、定时计划、高级。
![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/createTrigger.png)
![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/createTrigger2.png)

#### 基本
- **定时任务名称**：自定义定时任务的名称。
- **失败最大尝试次数**：若流程执行失败，系统会根据设置的数值进行自动尝试，默认为3次，设置范围为0~10次。
- **任务优先级**：任务优先级最低为0，最高为5000，优先级越高任务将越优先执行。
- **是否开启视频录制**：选择是否视频录制功能，开启后可在任务日志详情页中查看视频回放。

#### 定时计划
包含定时任务开始时间、结束时间、计划时间。
>**说明：**
>当用户配置完定时任务开始时间、计划时间、时区，会动态提示未来近3次的执行时间，以便用户第一时间验证设置的定时任务策略是否正确。
##### 1：有效期
- **定时任务开始时间**：到达开始时间之后，定时任务才会生效。
- **定时任务结束时间**：到达结束时间之后，定时任务不会再生成任务。
##### 2：计划时间
支持按分钟、按小时、按天、按周、按月、指定一个时间、按表达式。


- **按分钟**：以开始时间的 分钟为基准，并按照计划时间，循环触发任务执行。
>**说明：**
>按分钟，限制间隔需大于等于10分钟。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerMin.jpg)

- **按小时**：以开始时间的小时为基准，并按照计划时间，循环触发任务执行。
![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerHour.jpg)

- **按天**：以开始时间的天为基准，并按照计划时间，循环触发任务执行。
![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerDay.png)

- **按周**：以开始时间的小时为基准，并按照计划时间，循环触发任务执行。
![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerWeek.png)

- **按月**：以开始时间的月为基准，并按照计划时间，循环触发任务执行。支持“在当前月的正数第几天的几时几分”、“在当前月的倒数第几天的几时几分”、“在当前月的第几个星期几的几时几分”。

    在当前月的正数第几天的几时几分:
    ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerMonth1.jpg)

    在当前月的倒数第几天的几时几分:
    ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerMonth2.png)

    在当前月的第几个星期几的几时几分:
    ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerMonth3.png)

- **指定一个时间**：任务将在指定时间执行一次。
![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerOneTime.jpg)

- **按表达式**：根据cron表达式执行。
>**说明：**
>对于按照cron表达式执行定时计划任务，若了解cron表达式可自行根据规则编写，或通过云扩提供的cron表达式生成网站进行生成。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerCron.png)

#### 高级
定时任务的其他配置参数，机器人运行时的策略点，如时区等。

##### 1：时区
定时计划的所属时区。
>**说明：**
>时区，一般用于跨国公司场景，如IT运维在美国总部工作，可以设置中国子公司的业务流程按照时区[(UTC+08:00) 北京，重庆，香港特别行政区，乌鲁木齐]执行，也可以设置日本子公司的业务流程照时区[(UTC+09:00) 大阪，札幌，东京]执行。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerUTC.png)




### 第二步，单击“下一步”，进行执行目标及参数确认
- **组名称/机器人名称**：如果流程部署配置的执行方式为机器人组执行，此处展示队组称及备注；若流程部署配置的执行方式为指定机器人，则展示具体机器人名称及状态。

- **参数信息**：展示当前流程包中的参数值，若流程部署已对某参数值进行修改则此处将展示最新值。可在当前环节通过手动填写或导入资产进行重新赋值。
![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerStep2.png)

### 第三步，点击“保存”
完成定时任务填写后，点击“保存”，定时任务将在设置的开始/停用时间自动启用或停用。
>**说明：**
>
>- 流程部署的执行目标为指定机器人时：每次定时任务触发时每个机器人均会执行一次该流程。即关联了N个机器人，每次定时任务触发时将会生成N个流程任务。
>- 流程部署的执行目标为指定机器人组时：每次定时任务触发时该流程仅会执行一次，即生成一个流程任务在队列中动态分配。

## 查看及编辑定时任务详情

点击某一定时任务的“查看”按钮，即可查看对应的定时任务详情。点击“编辑”按钮后即可开始对定时任务进行编辑，完成后点击“保存”按钮即可。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerEdit.png)

## 查看定时任务的操作日志

点击某一定时任务的操作选项中的“查看日志”按钮，即可查看该定时任务的启用、停用、创建任务情况，便于对定时任务进行跟踪。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerEditLog.png)

## 启用/停用定时任务

你可以在定时任务列表中点击“操作”选项中的启用/停用按钮，对当前定时任务进行启用/停用操作。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/triggerDo.png)
