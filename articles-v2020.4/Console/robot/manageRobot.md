# 管理机器人

## 查看机器人列表

进入 **机器人管理**，你可以看到当前部门下的所有机器人。你可以选择切换部门，查看不同部门下的机器人。

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robotlist20210924.png)

## 新增机器人

点击“+新建”按钮，打开新增弹窗，填写机器人名称、标签、备注，并且选择机器人类型后，点击确定即可新建机器人。

> **说明：**
>
> 支持创建不同许可证类型的机器人，不同许可证类型的机器人，请参见 [许可证列表](../management/license/useLicense.md)。

 ![新建机器人](https://docimages.blob.core.chinacloudapi.cn/images/Console/createrobot20210628.png)

 新增成功后，系统将自动复制你的机器人连接字符串。你可以直接粘贴机器人连接字符串至客户端机器人，完成激活。详情见：[激活机器人](./../../Robot/license.md)。

> **说明：**
>
> 已创建的机器人，默认为“部门功能管理员”角色，可在“组织架构管理 > 数据权限配置 > 机器人权限”中查看点击“查看当前部门机器人权限”链接进行查看。

## 查看/编辑机器人详情

点击对应的机器人名称或“操作”栏中的“查看”选项，即可查看机器人详情信息。

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robotdetails20210924.png)

- **基本信息**：展示机器人的基本信息，通过点击“编辑”按钮，可对“基本信息”进行变更。
- **任务记录**：展示关联机器人的任务执行记录。
- **实时状态检测**：实时监控并展示当前机器人所在计算机的 CPU、内存、磁盘、网络等使用情况。
- **预警配置**：配置并展示当前机器人的预警阈值，当达到指定阈值时可发送邮件至指定邮箱或终止当前流程。

## 移除许可证

新创建的机器人默认拥有一个许可证，若当前机器人属于“已许可”状态，点击“操作”栏中的“移除许可”选项，即可移除当前机器人的许可证。

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/removelicense20210924.png)

## 分配许可证

新创建的机器人默认拥有一个许可证，若当前机器人属于“未许可”状态，点击“操作”栏中的“分配许可”选项，即可对当前机器人分配许可证。

 ![分配许可证](https://docimages.blob.core.chinacloudapi.cn/images/Console/assigntolicense20210924.png)

## 删除机器人

找到需要删除的机器人，在“操作”栏中，点击“删除”选项，可删除机器人。 被删除的机器人需要满足以下条件才可以删除成功：

- 机器人为断开状态
- 机器人当前在执行队列模块中，没有状态为等待和执行中的队列

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robot/robot/%E5%88%A0%E9%99%A4%E6%9C%BA%E5%99%A8%E4%BA%BA.png)
