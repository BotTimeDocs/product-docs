# 管理定时任务

## 定时任务
用户通过配置定时计划等，让流程编排按照既定的时间策略调度运行。

## 查看定时任务列表

在流程编排详情页中，单击任一流程编排的“定时任务”选项页，即可切换查看该流程编排名下所有的定时任务。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-list.png)

## 新建定时任务

1. 单击“+新建”

    在流程编排详情页的“定时任务”选项页中，单击“+新建” ，在弹出的新建对话框中，填写定时任务详情配置。新建页面包含 3 个部分：基础、定时计划、高级。

    ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-new.png)

    - **基本**

        - **定时任务名称**：自定义定时任务的名称。
 
    - **定时计划**

        包含定时任务开始时间、结束时间、计划时间。

        - **定时任务开始时间**：到达开始时间之后，定时任务才会生效。
        - **定时任务结束时间**：到达结束时间之后，定时任务不会再生成任务。

    - **计划时间**

        支持按分钟、按小时、按天、按周、按月、指定一个时间、按表达式。

        - **按分钟**：以开始时间的 分钟为基准，并按照计划时间，循环触发任务执行。

        > **说明：**
        >
        > 按分钟，限制间隔需大于等于 10 分钟。

        ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-min.png)

        - **按小时**：以开始时间的小时为基准，并按照计划时间，循环触发任务执行。

        ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-hour.png)

        - **按天**：以开始时间的天为基准，并按照计划时间，循环触发任务执行。

        ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-day.png)

        - **按周**：以开始时间的小时为基准，并按照计划时间，循环触发任务执行。

        ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-week.png)

        - **按月**：以开始时间的月为基准，并按照计划时间，循环触发任务执行。
        支持“在当前月的正数第几天的几时几分”、“在当前月的倒数第几天的几时几分”、“在当前月的第几个星期几的几时几分”。

            *在当前月的正数第几天的几时几分*:
            ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-month1.png)

            *在当前月的倒数第几天的几时几分*:

            ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-month2.png)

            *在当前月的第几个星期几的几时几分*:

            ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-month3.png)

        - **指定一个时间**：任务将在指定时间执行一次。

        ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-onetime.png)

        - **按表达式**：根据 cron 表达式执行。

        ![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-cron.png)

        > **说明：**
        >
        > 1，cron表达式，限制间隔需大于等于 10 分钟。
        > 2，对于按照 cron 表达式执行定时计划任务，若了解 cron 表达式可自行根据规则编写，或通过云扩提供的 cron 表达式生成网站进行生成。

2. 点击“保存”

    完成定时任务填写后，点击“保存”，定时任务将在设置的开始/停用时间自动启用或停用。

## 查看及编辑定时任务详情

点击某一定时任务的“查看”按钮，即可查看对应的定时任务详情。点击“编辑”按钮后即可开始对定时任务进行编辑，完成后点击“保存”按钮即可。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-view1.png)

## 启用/停用定时任务

你可以在定时任务列表中点击“操作”选项中的启用/停用按钮，对当前定时任务进行启用/停用操作。

![trigger](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-trigger-start.png)
