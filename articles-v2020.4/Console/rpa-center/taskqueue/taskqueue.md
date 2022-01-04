# 任务队列

## 概述

**任务队列** 主要用于监听业务数据并触发给相应的流程部署或机器人运行。

![任务队列](https://docimages.blob.core.chinacloudapi.cn/images/Console/taskqueue20211231.png)

## 一、新建任务队列

1. 在“任务队列”页面，单击“+新建”。
2. 在弹出的“新建”弹框中，输入队列相关的信息，单击“确定”。

    ![新建任务队列](https://docimages.blob.core.chinacloudapi.cn/images/Console/createtaskqueue20220104.png)

3. 已创建完成的任务队列，根据弹框提示可以对其关联相应的“流程部署”。

    ![关联流程部署](https://docimages.blob.core.chinacloudapi.cn/images/Console/taskqueuetip20220104.png)

## 二、关联流程部署

1. 在任务队列的“监听对象”详情页中，单击“新建”。

    ![新建监听对象](https://docimages.blob.core.chinacloudapi.cn/images/Console/bindworkflow20220104.png)

1. 选择对应的流程部署并关联至数据队列中。

    - 有新消息时触发：勾选时，表示有新消息时，则触发该任务队列。
    - 流程部署：选择需要关联的“流程部署”。
    - 消息关联至参数：当“流程部署”详情中有参数时，选择需要关联至的参数。
    - 消息移除：选择移除消息时前置条件。
    - 多个消息排队时：选择多个消息排队时的处理方式。

    ![关联流程部署](https://docimages.blob.core.chinacloudapi.cn/images/Console/dataqueue20220104.png)





