# 管理流程编排

## 流程编排列表
页面包含多种操作，如新建、查看、定时任务、复制、删除、执行、批量操作。
![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-list.png)


## 新建流程编排

1. 在流程编排页面中，点击“新建”按钮后，即可开始新建：

    ![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-new1.png)
    ![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-new2.png)

2. 从左侧拖拽一个流程部署，作为其中一个节点，可以调整节点顺序
![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-new3.png)

3. 编辑流程部署的参数：支持导入和手动录入2种方式
![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-paramters.png)
> **说明：**
> 流程有多种触发启动的场景，每个场景都有自己的一套参数值（默认值为源流程部署初始设置）。触发场景继承了源流程部署的基本信息（除了参数值），源基本信息变化，会同步到各个触发场景，而源流程部署的参数值的变化，不会同步并影响各个场景的参数值。



4. 保存流程编排
![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-new-success.png)

5. 复制流程编排
![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-copy.png)


## 查看流程编排详情

单击流程编排列表页中的“流程编排名称”。

![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-view1.png)
![流程编排](https://docimages.blob.core.chinacloudapi.cn/images/Console/0528flowsquence-info.png)
- **基本信息**：展示当前流程编排的基本信息，单击“编辑”按钮，可变更流程编排的基本信息。
- **定时任务**：展示当前流程编排的定时任务列表，参见 [管理定时任务](./triggerFlowSequence.md)。
- **执行记录**：展示当前流程编排的执行记录，参见 [执行记录](./flowSequenceHistory.md)。


## 流程编排启动方式
包含2种启动方式：

1. 定时任务：通过定时方式触发流程编排，来串行执行的多个流程任务。
2. 手动执行：可以通过手动方式触发流程编排，来串行执行的多个流程任务。


## 搜索流程编排

在页面左上角的搜索框中，输入“流程编排名称”、“标签”信息的关键字，可模糊查找对应的流程编排。

## 删除流程编排

点击所选的流程编排“操作”栏中的“删除”选项，即可删除相应的流程部署。

## 批量操作

勾选需要批量操作的“流程编排”，单击右上角的“批量操作”，可对其进行删除操作。
