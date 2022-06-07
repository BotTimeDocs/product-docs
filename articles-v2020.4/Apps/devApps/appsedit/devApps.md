# 应用编辑器概述

开发者可以在应用编辑器内，通过零代码开发功能设计与开发应用，并对应用进行预览、保存与发布操作。

## 应用编辑器入口

打开站点，单击“应用管理”菜单，在进入的应用列表页面的操作栏中，选择“编辑”选项，即可设计与开发当前应用。

![编辑应用](https://docimages.blob.core.chinacloudapi.cn/images/Kris/editapp.jpg)

## 应用编辑器简介

应用编辑器，根据布局分为以下三大部分部分，分别是

![布局](https://docimages.blob.core.chinacloudapi.cn/images/Kris/layout.png)

1. 顶部导航栏：提供使用应用编辑器的基本功能。
2. 左侧导航区：支持应用页面、业务逻辑、数据以及权限的新建与管理。
3. 编辑区：对应用页面、业务逻辑、数据以及权限进行编辑。

### 顶部导航栏

顶部导航栏提供了使用应用编辑器的基本功能。

![顶部导航栏](https://docimages.blob.core.chinacloudapi.cn/images/Kris/topbar.jpg)

1. 返回：返回控制台。
2. 预览：开发过程中可快速预览应用。
3. 保存：将编辑器当前内容进行保存。
4. 发布：开发并测试完成的应用可发布到控制台-我的应用，供业务人员使用。
5. [变量管理](./variable.md)：管理应用中的变量。通过将变量与页面组件某个属性进行绑定，可以使该属性动态变化。


### 左侧导航区

左侧导航区主要是针对应用页面、业务逻辑、数据以及权限的新建与管理。根据不同的导航可进入到不同的视图。

### 页面

[页面](./page/PageSetting.md)主要管理应用的页面和页面组件等。

![页面](https://docimages.blob.core.chinacloudapi.cn/images/Kris/pagenavigation.jpg)

1. 页面：管理应用内所有页面，并支持新建、删除和设置为首页等。
2. 组件：展示官方的页面组件库。
3. 大纲：展示当前页面完整的组件大纲，便于区分组件层级。

### 动作流

[动作流](./action-flow/action-flow.md)主要管理应用的动作流和动作流组件等，用于处理应用业务逻辑。

![动作流](https://docimages.blob.core.chinacloudapi.cn/images/Kris/actionflownav.jpg)

1. 动作流：管理当前页面关联的动作流，并支持新建、删除等。
2. 组件：展示官方的动作流组件库。

### 数据源

[数据源](./datamodel/about-datamodel.md)主要管理应用内的所有数据源，用于访问与更新应用数据。

![数据源](https://docimages.blob.core.chinacloudapi.cn/images/Kris/datasourcenav.jpg)

### 角色权限

[角色权限](./rolepermissions.md)主要管理应用内角色，用于控制应用页面和数据的访问权限。

![角色权限](https://docimages.blob.core.chinacloudapi.cn/images/Kris/rolenav.jpg)


### 编辑区

编辑区用于对应用页面、业务逻辑、数据以及权限进行编辑。根据不同的左侧导航可进入不同的编辑区。

#### 页面设计器

在页面设计器里，通过简单的拖拉拽组件即可快速搭建应用页面。

![页面设计器](https://docimages.blob.core.chinacloudapi.cn/images/Kris/pageeditor.jpg)

1. 设计器：展示页面样式，支持拖拽、删除组件等操作。
2. 属性设置：对页面组件的数据属性进行静态设置，或与变量、表达式等进行动态绑定。
3. 事件处理：对页面组件进行事件绑定与监听，实现单击跳转页面、消息通知等操作。

#### 动作流编辑器

在动作流编辑器里，通过简单的拖拉拽组件即可快速搭建应用业务逻辑。

![动作流编辑器](https://docimages.blob.core.chinacloudapi.cn/images/Kris/actionfloweditor.jpg)

1. 编辑器：展示业务逻辑处理，支持拖拽、删除组件等操作。
2. 属性设置：对动作流、动作流组件的数据属性进行静态设置，或与变量、表达式等进行动态绑定。
3. 动作流变量：管理动作流内部变量，实现动作流内的数据传递。

