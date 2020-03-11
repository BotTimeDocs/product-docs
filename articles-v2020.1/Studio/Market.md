# 云扩市场
云扩市场中含有组件市场和流程市场。

**组件市场**是用来丰富开发者组件库的，当您在开发的过程当中发现当前组件无法满足您的需求，您可以从组件市场查找并下载您需要的组件包来进行自动化项目的创建。

**流程市场**就是可以把通用的流程发布到流程市场中，为您提供共享流程库，可进去自行下载需要的参考流程。

## 组件市场 
组件市场中的组件包可以链接到指定的项目中，作为该项目的依赖项存在。在每个项目中，只有至少存在一个引用时，才会设置依赖项。 

如果需要添加依赖项，您可以单击“组件市场”选择相应组件包进行安装。

![组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/activityMarket.png)

>注意：
>
>已安装的依赖项仅适用于当前的项目，并且在botTimeRPA.json文件中可以看到每个项目的依赖项列表。

工作目录窗口显示项目中安装的组件包以及所安装组件包的版本号。

![工作目录](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/dependence.PNG)

组件窗口中则展示了每个组件包中所包含的所有组件，使用时直接拖拽到工作流中使用即可。

![组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/activities-dependence.PNG)

在组件市场窗口中，还存在两个其他分类--已安装组件及本地组件。
* **已安装组件**仅针对当前项目存在，仅显示当前项目已安装的组件包，通过该页面可以管理项目中的依赖项。

![已安装组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/installedActivities.PNG)

* **本地组件**最为重要的是，当您处于无网络或其他无法连接到组件市场的情况时，您依然可以使用曾经下载过的组件包，将他们应用于您的自动化项目中。

![本地组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/localActivities.PNG)


### 管理依赖项 
在组件市场中，可查看依赖项的版本，同时可对依赖项进行添加、更新和删除。
要管理依赖项，右击工作目录窗口中的依赖项类别，打开菜单，单击“管理”。或者单击工具栏下的设计->组件市场。这都将打开“组件市场”窗口。
1. 对于未添加依赖项的项目，只需通过搜索相应的组件包，找到并安装它们，即可将所需组件添加到项目中。 
2. 对于已添加依赖项的项目，通过已安装组件页面，单击删除即可删除该依赖项，要想更新组件包，只需单击更新按钮。

## 流程市场

流程市场存放了各种各样的自动化流程，您可以下载某些场景的自动化项目进行参考学习或进行复用。

如果需要查看相关流程，您可以通过点击工具栏的设计->流程市场，选择流程来进行下载。 

![流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/flowMarket.PNG)

>注意：
>
>下载的自动化流程将作为一个独立的项目存在。

若流程是您自己开发的，需要发布到流程市场中进行共享，您可以通过点击工具栏的发布->流程市场进行发布流程。

![发布到流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/publishToFlowmarket.PNG)

### 管理流程市场

通过管理流程市场，您可以添加您的私有化流程市场，详细步骤请咨询我们的工作人员。

![管理流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/manageFlowmarket.PNG)

 
