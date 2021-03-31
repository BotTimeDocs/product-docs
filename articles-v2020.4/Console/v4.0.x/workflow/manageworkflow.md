# 管理流程部署

## 新建流程部署

1. 在流程部署页面中点击“新建”按钮后即可开始新建：

    - 填写流程部署基本信息，选择对应的流程包以及流程包版本号。
    - 设置失败最大尝试试次数，流程执行失败后将按照该次数自动进行重试。
    - 设置任务优先级（1-5000）：优先级越高该任务将被越先执行

    ![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/%E6%96%B0%E5%BB%BA%E6%B5%81%E7%A8%8B%E9%83%A8%E7%BD%B21.1.png)

    - 对流程包中的参数进行赋值：

        - 手动赋值：填写需要进行赋值的参数值即可

        - 导入资产：点击“导入资产”即可选择在资产管理页面中预先存储的资产进行赋值

    ![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/%E6%96%B0%E5%BB%BA%E6%B5%81%E7%A8%8B%E9%83%A8%E7%BD%B2%E7%AC%AC%E4%B8%80%E9%A1%B5%E8%A1%A5%E5%85%85.png)

    ![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/%E6%96%B0%E5%BB%BA%E6%B5%81%E7%A8%8B%E9%83%A8%E7%BD%B2-%E5%AF%BC%E5%85%A5%E8%B5%84%E4%BA%A7.png)

2. 点击“下一步”开始配置机器人执行目标，选择指定队列执行/指定机器人执行

    - 执行队列执行：从该资源组下已创建的队列进行选择；

    ![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow3.png)

    - 指定机器人选择: 展示该资源组下所有的机器人，通过勾选选定，支持按照名称及标签进行搜索。

    ![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow4.png)

3. 点击保存即完成流程部署新建，点击【保存并设置触发器】即开始快捷配置定时计划。（详见“定时计划管理”）

## 查看流程部署配置信息

点击流程部署中的“配置”按钮即可查看流程部署的配置信息

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow5.png)

## 基本配置及参数修改

在流程部署的“配置”页面中点击“编辑”按钮即可对基本配置信息及参数信息进行修改，修改完成后点击“保存”按钮即可。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow6.png)

## 删除流程部署

点击所选的流程部署操作选项中的“删除”按钮即可删除相应的流程部署。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow7.png)
