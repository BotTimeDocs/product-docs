# 云扩市场
云扩市场包括组件市场和流程市场：

**组件市场**提供大量云扩科技和合作伙伴开发的自动化组件和人工智能组件。当流程设计者无法在基本组件中找到适合业务需要的组件时，可尝试到组件市场搜索，下载到项目中即可使用，无需再自己开发。

**流程市场**提供已经设计好的适应特定场景的流程以及流程模板，下载即可使用。也可以参考已有的流程，修改设计使其成为适合企业业务需要的自定义流程，大大提高流程编辑。

此外，也支持企业用户部署私有化市场，具体方法请[联系我们](https://www.encoo.com/apply)，竭诚为您服务。

## 组件市场 
组件市场中的组件包可以链接到指定的项目中，作为该项目的依赖项存在。

### 下载、安装与使用

![组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/M-0.png)

1. 在“项目面板”面板中双击打开将要被安装组件的目标项目
2. 在工具栏点击“组件市场”打开组件市场窗口
3. 在搜索文本框输入关键字查找组件，例如“云扩”
4. 选中组件并点击“下载”图标

    ![组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/M-1.png)

5. 在“安装组件”窗口点击“确定”将此组件安装至项目中

    ![组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/M-2-0.png)

6. 在项目的“依赖项”中可查看下载的组件信息

    ![组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/M-2.png)

    >注意：
    >
    >在每个项目中，只有至少存在一个引用时，才会设置依赖项。
    >
    >已安装的依赖项仅适用于当前的项目，并且在project.json文件中可以看到每个项目的依赖项列表。

7. “组件面板”的“扩展”目录包含了从“组件市场”下载的所有组件，直接拖拽到流程中即可使用

    ![组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/M-3.png)


### 已安装组件

在组件市场窗口中，还存在一个其他分类：已安装组件

* **已安装组件**仅针对当前项目存在，仅显示当前项目已安装的组件包，通过该页面可以管理项目中的依赖项。

    ![已安装组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/installedActivities.PNG)
<!-- 
* **本地组件**最为重要的是，当你处于无网络或其他无法连接到组件市场的情况时，你依然可以使用曾经下载过的组件包，将他们应用于你的自动化项目中。

    ![本地组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/localActivities.PNG) -->

### 管理依赖项

在组件市场中，可查看依赖项的版本，同时可对依赖项进行添加、更新和删除。
要管理依赖项，右击项目面板中的依赖项类别，打开菜单，点击“管理”。或者点击“市场”->“组件市场”。这都将打开“组件市场”窗口。

1. 对于未添加依赖项的项目，只需通过搜索相应的组件包，找到并安装它们，即可将所需组件添加到项目中。 
2. 对于已添加依赖项的项目，通过已安装组件页面，点击删除即可删除该依赖项，要想更新组件包，只需点击更新按钮。

## 代码市场 
代码市场中的代码包可以下载到编辑器中，主要用于执行代码组件及表达式编辑器中。与组件市场不同，其在组件面板不可见，如果需要使用，可在编辑区域底部的**导入**中进行引用。

### 下载、安装与使用

![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-0.png)

1. 在“项目面板”面板中双击打开将要被安装代码包的目标项目
2. 在工具栏点击“代码市场”打开代码市场窗口
3. 在搜索文本框输入关键字查找代码包，例如“queue”
4. 选中代码包并点击“下载”图标

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-1.png)

5. 在“安装组件”窗口点击“确定”将此代码包安装至项目中

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-2.png)

6. 如果该代码包需要接受许可证，则会弹出“接受许可证”窗口，接受则继续下载，拒绝则不下载。

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-3.png)

7. 在项目的“依赖项”中可查看下载的代码包信息

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-4.PNG)

    >注意：
    >
    >在每个项目中，只有至少存在一个引用时，才会设置依赖项。
    >
    >已安装的依赖项仅适用于当前的项目，并且在project.json文件中可以看到每个项目的依赖项列表。

8. 编辑区域的“导入”中可以搜索到下载的代码包，搜索后点击即可引用到项目中。

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-5.PNG)


### 已安装代码包

在代码市场窗口中，还存在一个其他分类：已安装代码包

* **已安装代码包**仅针对当前项目存在，仅显示当前项目已安装的代码包，通过该页面可以管理项目中的依赖项。

    ![已安装代码包](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-6.PNG)

### 管理依赖项

在代码市场中，可查看依赖项的版本，同时可对依赖项进行添加、更新和删除。
要管理依赖项，右击项目面板中的依赖项类别，打开菜单，点击“管理”。或者点击“市场”->“代码市场”。这都将打开“代码市场”窗口。

1. 对于未添加依赖项的项目，只需通过搜索相应的代码包，找到并安装它们，即可将所需代码包添加到项目中。 
2. 对于已添加依赖项的项目，通过已安装代码包页面，点击删除即可删除该依赖项，要想更新代码包，只需点击更新按钮。

## 流程市场

流程市场内置了丰富的适应特定场景的流程以及流程模板，可下载后参考学习或进行复用。

### 下载与使用 

![流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/FM-0.png)

1. 在流程列表选择想要下载的流程
2. 点击“下载”图标

    ![流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/FM-1.png)

3. 在“新建项目”窗口输入“项目名称”，点击“创建”将创建一个新的项目

    ![流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/FM-2.png)

    >注意：
    >与下载组件不同的是，流程下载后将作为一个独立的项目存在

4. 在项目面板面板即可查看以新项目名称命名的流程

    ![流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/FM-3.png)

## 管理市场

在“组件/流程市场”窗口点击“管理市场”可创建本地或基于特定网络的私有市场

![ManagementMarket](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/MarketManagement.png)

### 本地私有市场

在“市场地址”文本框指定本地文件夹并保存后即可加载本地组件

### 部署基于特定网络的私有市场

部署基于特定网络的私有市场的详细步骤您可以拨打 400-639-2198 联系您的专属顾问，我们将竭诚为您提供帮助！也可以访问[此页面](https://www.encoo.com/apply)页面并留下您的联系方式，我们的工作人员会在1-2个工作日联系您。

