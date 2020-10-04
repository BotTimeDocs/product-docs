## 应用管理
进入**应用管理**，你可以看到当前资源组下的所有被发布的应用。你可以选择切换**资源组**，查看不同资源组下的应用。

## 查看应用

应用列表将罗列所有被发布的应用及应用当前状态。
**启用**:指当前应用已被上架，资源组下用户可以通过访问工作台站点的**我的应用**查看并运行该应用
**禁用**：指当前应用为下架状态，用户不可见

启用的应用将会标记他当前启用的版本号。
你可以点击应用名称查看应用详情。
 ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/manageapps.png)

## 查看应用详情
点击应用名称，打开应用详情。
在应用详情，你可以查看应用当前版本和历史版本，当前启用版本会在版本号处显示**当前**标记。
你也可以在详情页试用应用当前版本。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/appsdetail.png)

点击**查看更多版本**查看应用其他版本
箭头标记的为当前预览版本，你可以通过点击版本号切换当前预览版本。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/appsdetail2.png)

当你想要切换当前应用启用的版本时，通过**查看更多版本**切换到想要启用的版本详情，在详情内点击**切换到当前版本**，即可将应用启用版本切换至当前选定版本。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/appsdetail3.png)

注意：禁用应用因未被上架，所以不存在当前启用版本。

## 启用应用
对于**禁用**状态的应用，你可以通过列表或详情的启用按钮启用应用。
当应用在列表被启用时，默认启用应用内最新版本。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/activeapps1.png)
当应用在详情被启用时，默认启用当前详情选择版本。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/activeapps2.png)

## 禁用应用
对于**启用**的应用，你可以在和你可以通过列表或详情的禁用按钮启禁用用。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/inactiveapps1.png)
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/inactiveapps2.png)

## 删除应用
你可以选择删除单个版本或整个应用。

当你删除整个应用时，应用下的所有版本将被删除，工作台站点中的应用的原始开发包也将被删除。

### 删除应用
进入应用管理页面，找到要删除的应用，点击删除，二次确认后即可删除。
![package](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/deleteApps.png)



### 删除应用版本
进入应用管理页面，找到要删除的版本所在的应用.
在应用详情中点击，查看版本。
找到要删除的版本，点击删除，即可删除。
![package](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/deleteApps1.png)
删除版本需满足以下条件：
 - 版本非”当前”状态