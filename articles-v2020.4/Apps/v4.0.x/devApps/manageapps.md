# 应用管理

进入 **应用管理**，你可以看到当前部门下的所有已创建的应用。你可以选择切换 **部门**，查看不同部门下的应用。

## 新增应用

选择“应用管理”菜单 ，进入应用管理列表页面，单击“+新增”，在弹出的“新增应用”弹框中，创建应用。

![创建应用](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/createapp20210426.png)

## 查看应用

应用列表将展示所有已创建的应用及应用当前状态。

> **说明：**
>
> 启用的应用将会标记它当前启用的版本号。

![查看应用列表](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/manageapps20210426.png)

## 查看应用详情

点击应用名称，即可打开应用详情相关信息。在应用详情页面，你可以查看应用的“版本信息”及“数据权限信息”。

- **版本管理**：展示当前应用的版本历史信息。当前启用版本会在版本号处显示“当前”标记，你也可以在详情页试用应用当前版本。

    > **说明：**
    >
    > 禁用应用因未被上架，所以不存在当前启用版本。

    ![版本管理](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/appversion20210426.png)

- **数据权限配置**：展示当前应用的所在部门的权限信息。

    ![数据权限](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/datagrant20210426.png)

## 启用应用

启用应用，指当前应用已被上架，部门下用户可以通过访问“应用中心 > 我的应用”，查看并运行使用该应用。对于 **停用** 状态的应用，你可以通过应用列表或详情页中的“启用”按钮，启用应用。

> **说明：**
>
>- 当应用在列表中被启用时，默认启用应用内最新版本。
>- 当应用在详情页中被启用时，默认启用当前详情页中的选择版本。

![启用应用](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/enableapps20210426.png)

## 停用应用

停用应用，指当前应用为下架状态，用户不可见。对于 **启用** 的应用，你可以在和你可以通过列表页或详情页中的“停用”按钮，停用应用。

![停用应用](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/stopapps20210426.png)

## 删除应用

你可以选择删除单个版本或整个应用。

- 当删除整个应用时，应用下的所有版本将被删除，应用的原始开发包也将被删除。

    ![删除整个应用](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/deleteapps20210426.png)

- 当删除单个版本时，需在应用详情的“版本管理”中选择对应的版本进行删除。
  
    > **说明：**
    >
    > 处于“当前”启用状态的版本，无法删除。

    ![删除单个版本](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/deleteappversion20210426.png)

## 编辑应用

进入已创建应用的编辑模式，详情请参见 [应用开发模式](../devApps.md)。

![编辑应用](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/devapps20210426.png)

## 复制应用

复制当前已创建的应用，以方便开发者克隆一个完全一样的应用。

![复制应用](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/copyapps20210426.png)
