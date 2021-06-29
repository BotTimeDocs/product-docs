# 手动执行流程

除了通过任务计划定时创建流程任务之外，你也可以手动立即执行流程:

1. 在“流程部署”页面中选择要立即执行的流程部署，点击“操作”选项中的“执行”按钮。

    ![workflow](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow8.png)

2. 在“流程执行”弹窗中，可以对失败最大尝试次数、参数值进行重新赋值，确认无误后点击“执行”按钮，可生成对应的任务执行。可在“流程部署 > 任务列表”中查看对应任务的执行情况。

    ![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow9.png)

    >**说明：**
    >
    >- 流程部署的执行目标为指定机器人时：每个机器人均会执行一次该流程，即关联了N个机器人将会生成N个流程任务。
    >- 流程部署的执行目标为指定队列时：该流程仅会执行一次，即生成一个流程任务在队列中动态分配。