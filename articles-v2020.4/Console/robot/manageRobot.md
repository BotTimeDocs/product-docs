# 管理机器人

## 查看机器人列表

进入 **机器人管理**，你可以看到当前部门（资源组）下的所有机器人。你可以选择切换 **资源组**，查看不同资源组下的机器人。

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robot/robot/%E6%9C%BA%E5%99%A8%E4%BA%BA%E4%B8%BB%E9%A1%B5.png)

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

## 查看机器人详情

点击对应的机器人名称即可查看机器人详情信息

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robot/robot/%E6%9F%A5%E7%9C%8B%E5%8F%8A%E7%BC%96%E8%BE%91%E6%9C%BA%E5%99%A8%E4%BA%BA%E8%AF%A6%E6%83%85-1.png)

## 编辑机器人信息

在机器人详情页面中点击“编辑”按钮即可开始对机器人信息进行编辑，编辑完成后点击“保存”即可。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robot/robot/%E6%9F%A5%E7%9C%8B%E5%8F%8A%E7%BC%96%E8%BE%91%E6%9C%BA%E5%99%A8%E4%BA%BA%E8%AF%A6%E6%83%85-2.png)

点击对应的机器人名称即可查看机器人详情信息。

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robot/editrobot.png)

在机器人详情页面中点击“编辑”按钮，可开始对机器人信息进行编辑，编辑完成后点击“保存”。

## 移除许可证

新创建的机器人默认拥有一个许可证，若当前机器人属于“已许可”状态，点击操作中的“移除许可”按钮即可移除当前机器人的许可证。

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robot/robot/%E7%A7%BB%E9%99%A4%E8%AE%B8%E5%8F%AF%E8%AF%81.png)

## 分配许可证

新创建的机器人默认拥有一个许可证，若当前机器人属于“已许可”状态，点击操作中的“移除许可”按钮即可移除当前机器人的许可证。

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robot/robot/%E7%A7%BB%E9%99%A4%E8%AE%B8%E5%8F%AF%E8%AF%81.png)

## 删除机器人

找到需要删除的机器人，在操作栏中，点击“删除”，可删除机器人。 被删除的机器人需要满足以下条件才可以删除成功：

- 机器人为断开状态
- 机器人当前在执行队列模块中，没有状态为等待和执行中的队列

 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Console/robot/robot/%E5%88%A0%E9%99%A4%E6%9C%BA%E5%99%A8%E4%BA%BA.png)
