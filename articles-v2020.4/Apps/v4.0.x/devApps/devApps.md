# 应用开发模式

开发者可以在该模式下，通过应用的零代码开发功能设计与开发应用，并对应用进行预览、保存与发布操作。

## 应用开发模式入口

打开站点，单击“应用管理”菜单，在进入的应用列表页面的操作栏中，选择“编辑”选项，即可设计与开发当前应用。

![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/devapp20210426.png)

## 应用开发模式简介

应用编辑器，根据布局分为如下几部分，分别是

![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/paneluserinterface20210422.png)


1. 菜单导航栏：ViCode编辑模式由以下几个区域组成。

    - [大纲页面](../devApps/appsedit/PageSetting.md)：管理应用内的页面、数据源和代码。
    - [设置页面](../devApps/appsedit/BasicSetting.md)：管理应用的全局设置。
    - [全局变量页面](../devApps/appsedit/variable.md)：展示和管理应用的变量。
    - [数据页面](../devApps/appsedit/datasource.md)：管理应用中的数据源，包括 SQL 和 Restful API。
    - [代码页面](../devApps/appsedit/executecode.md)：管理应用中的代码，包括 JavaScript 代码。
    - [连接器映射关系页面](../devApps/appsedit/connector.md)：配置测试连接器与生产连接器的映射关系。
2. 目录树区域：在开发应用过程中用到的页面、数据源、代码等大纲目录。
3. [组件库区域](../devApps/appsedit/component/aboutComponent.md)：通过选择不同的组件，创建页面元素，开发应用。
4. 模拟界面（即，画布区域）：用于向用户展示编辑的界面样式，用户可以在模拟界面选中/拖拽移动/删除组件。

   >**小技巧：**
   >
   >在模拟界面中，键盘按下空格键时，鼠标呈现一只小手形状的手势，可以拖拽画布。

5. 属性区域：用于组件对本身的属性进行设置，不同组件拥有不同的属性栏。属性栏将根据模拟界面选中的组件进行切换。
6. 顶部导航：用于预览、发布、设置主题等全局性的应用的操作。