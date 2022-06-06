# 动作流

## 概述

**动作流** 用于自定义应用业务逻辑，用户能够通过拖拉拽组件的方式，对一系列动作进行编排，简单快速搭建业务流程，帮助完成复杂交互。在动作流内，你可以进行打开新页面、消息通知等操作。

## 新建动作流

1. 动作流视图顶部栏单击“+”按钮，将会打开一个“新建动作流”弹窗
2. 在弹窗内输入动作流名称，并选择动作流所属页面
3. 单击“确定”，即可在应用内添加一个空白动作流

    ![新建动作流](https://docimages.blob.core.chinacloudapi.cn/images/Kris/addactionflow.jpg)

>**说明：**
>
>动作流命名规范：
>
>1. 当前所属页面内不可重名
>2. 仅支持输入汉字、字母、数字和下划线，且不能以数字开头

## 编辑动作流

1. 动作流视图选择并打开一个动作流
2. 从动作流组件视图拖入动作流组件到动作流编辑器
3. 配置动作流组件属性

    ![编辑动作流](https://docimages.blob.core.chinacloudapi.cn/images/Kris/editactionflow.jpg)

## 运行动作流

当动作流开发完成后，你可以通过在动作流编辑器顶部栏单击“运行”来运行动作流，查看运行结果。

![运行动作流](https://docimages.blob.core.chinacloudapi.cn/images/Kris/runactionflow.jpg)

## 调用动作流

1. 在 ViCode 的页面视图，拖入页面组件到页面设计器里
2. 选择需要触发动作流的组件，在“事件”属性中，单击“添加事件”，添加相应事件
3. 单击“添加动作”，选择“执行动作流”并关联已创建完成的动作流

    ![调用动作流](https://docimages.blob.core.chinacloudapi.cn/images/Kris/invokeactionflow.jpg)
