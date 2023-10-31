# 管理3、《流程运行管理》

<br> 

>  导读 : 
> 
> 本章指南，重在介绍控制台流程调度的三个概念:触发器(流程触发方式)、自动化流程、执行资源调度；
> 
> 流程运行权限、运行时机器人与计算机与监控计算机性能的监控、以及对流程的监控。
> 

<br> <br> <br> 

## 一、控制台流程调度

控制台可以灵活实现对自动化流程的调度、管理，支持各种策略可以实现大规模流程调度，集群式机器人协同。

理解控制台对自动化流程的调度主要有三个概念组成：1. 触发器；2.自动化流程；3. 执行资源。

1. 触发器：即使自动化流程运行的触发条件，控制台支持人工方式触发执行、定时任务触发执行、监听数据队列消息触发;

2. 自动化流程：即流程包;

3. 执行资源：即自动化流程的运行环境，主要有机器人、机器人组；

</br>

## 二、触发器 ——流程触发方式介绍

### 方式1：手动
通过控制台点击立即执行， 或通过控制台API调取执行。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-07.png"/>

</br></br>


### 方式2：定时

通过配置定时任务，来实现规律性的调度执行；单个流程部署可以设置多个定时任务，实现灵活的定时调度；

</br>

**(1) 定时任务开始、结束时间:**

设定定时计划的生效时间，定时任务是从定时任务开始时间才开始监听时间变化，根据计划触发调度执行。 

同理到达定时任务结束时间后，本定时任务停止监听时间变化，定时任务停止。

</br>

**(2) 计划时间:**

设定定时计划，控制台支持灵活的定时计划。

</br>

可以实现 按照分钟间隔、按照小时间隔、按天、按周、按月或者指定一个时间执行、按照linux cron表达式调度执行；
</br>

* 按分钟： 可以设置每间隔 x分钟调度执行一次；

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-08.png"/>



* 按小时： 可以设置每间隔x小时，在该小时对应的第x分钟调度执行一次；

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-09.png"/>


* 按天： 可以设置每间隔x天，在当天的xx小时xx分执行调度一次；

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-10.png"/>


* 按周： 可以设置每间隔x周，在当周的周x的第xx小时xx分执行调度一次；

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-11.png"/>


* 按月：</br>
   1，可以设置每间隔x月，在当月的第xx天的第xx小时xx分执行调度一次；</br>
   2，可以设置每间隔x月，在当月的倒数第xx天的第xx小时xx分执行调度一次；</br>
   3，可以设置每间隔x月，在当月的第x个周x执行调度一次；</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-12.png"/>


* 指定一个时间：指定一个时间点，执行一次；

* 按表达式： 可以设置Linux Cron表达式，实现基于Cron表达式的执行调度；

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-13.png"/>

<br><br><br>

### 方式3：任务队列
可以通过设置控制台的任务队列，关联需要执行的流程部署，设置处理队列消息的策略实现对消息的监听。

在流程中可以使用发送消息组件，发送消息到任务队列，实现按照消息队列触发调度。

任务队列消费消息支持多种策略：
1. 多个消息排队时，立即触发新的流程部署；
2. 多个消息排队时，排队等待流程上一个流程部署执行结束；
3. 多个消息排队时，如已有对应部署在执行，则抛弃排队的消息；

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-14.png"/>


<br><br><br>

## 三、执行资源调度

执行资源最小单位是机器人，多个机器人可以设置为一个机器人组； 

</br>

* **任务调度方式1：指定到多个机器人**

创建流程部署，可以指定到多个机器人来执行，调度时候，可以根据指定的机器人列表寻找一个可用机器人来执行自动化流程；</br>
    
</br>指定多个机器人执行，当执行资源被占用时，可灵活设置以下调度策略：

1. 等待可用资源ready后，执行；
2. 放弃本次调度

</br></br>

* **任务调度方式2：指定到机器人组**</br>

创建流程部署，可以指定到一个机器人组，调度时候，可以根据指定的机器人组中寻找一个可用机器人来执行自动化流程；</br>

指定一个机器人组，当所有执行资源被占用时，可灵活设置以下调度策略：</br>
1. 等待可用资源ready后，执行；
2. 放弃本次调度

</br>
</br>
</br>


## 四、流程运行权限

运行权限可以分为以下三类

1. 以管理员执行：即执行时会使用管理员权限
2. 以非管理员执行：即执行时不使用管理员权限
3. 与编辑器启动权限一致</br>

</br>

* 如果是控制台下发的流程，默认是非管理员（即选择更安全的方式）</br>

* 如果是在机器人上执行，则取决于Robot.exe进程的权限，通常的以管理员权限执行的</br>

流程执行权限，取决于编辑器中对于流程包的设置，编辑器中设置项目的运行权限位置在，项目名右键->项目设置->常规->运行权限</br>

</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-15.png"/>


<br><br><br>

## 五、运行监控入门

### (1) 机器人与计算机
一个安装了机器人的计算机，其中每个windows用户能够连接到控制台上不同的机器人，即一个计算机上会存在多个机器人。

</br>

### (2) 监控计算机性能
在运维监控工作开始前，首先需要确定监控的目标，也就是确定一个具体的计算机作为监控对象。一般来说，在控制台中找到指定的计算机进行监控，有以下两个途径：
</br>

* 途径1：根据机器人去寻找
</br>在已知要监控某个机器人所在计算机的场景下，首先需要进入机器人管理页面，通过查询功能，找到该机器人

</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-16.png"/>


</br></br>

在找到指定的机器人后，点击计算机列的超链接，即可跳转到该计算机的详情页面。

</br>

> **注意：**
> 这种方式需要保证机器人与控制台已建立了连接，如果是断开状态，则无法进行跳转。

</br></br>

* 途径2：根据计算机去寻找
</br>在已知需要监控的计算机信息时，可以直接前往计算机管理页面进行查询，找到要监控的计算机

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-17.png"/>


</br></br>

在找到指定的机器人后，点击计算机列的超链接，即可跳转到该计算机的详情页面。

在进入计算机详情页后，有三个选项卡，能够分别从不同的维度来查看该计算机当前的情况

* 维度1：基本信息，包含以下计算机信息</br>

    1. 硬件规格（CPU型号、内存容量、硬盘容量）</br>
    2. 软件状态（操作系统、系统运行时长、内存使用量、硬盘使用量）

</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-18.png"/>



</br></br>

* 维度2：机器人，当前部门下已连接到当前控制台的机器人列表

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-19.png"/>

</br></br>

* 维度3：实时监控，当前计算机的实时信息图表，包含以下内容：</br>
1. CPU使用率
2. 内存使用率
3. 磁盘读写
4. 网络传输

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/lmx-20.png"/>


<br><br><br>

## 六、流程监控
开发并上架 一个ViCode 应用，“已上架”的ViCode 应用，会占用许可，即当上架一个应用，则”许可证管理“下许可的“已绑定量”会+1。
同时，用户亦可在”许可证管理“下移除应用，进而收回一个许可。
</br>

关于总体监控，详见[总体监控产品说明](https://academy.encoo.com/zh-cn/wiki/Console/dashboard/dashboard.md?_v=v2020.4) </br>

关于机器人监控，详见[机器人监控产品说明](https://academy.encoo.com/zh-cn/wiki/Console/dashboard/RobotDashboard.md?_v=v2020.4) </br>

关于机器人组监控，详见[机器人组监控产品说明](https://academy.encoo.com/zh-cn/wiki/Console/dashboard/QueueDashboard.md?_v=v2020.4) </br>

关于机器人运行统计表，详见[机器人运行统计表产品说明](https://academy.encoo.com/zh-cn/wiki/Console/dashboard/dashboard2.md?_v=v2020.4) </br>

关于用户流程统计表，详见[用户流程统计表产品说明](https://academy.encoo.com/zh-cn/wiki/Console/dashboard/dashboard3.md?_v=v2020.4) </br>