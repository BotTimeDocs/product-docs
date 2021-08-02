# 关于组件

在页面设置的下方可以找到组件栏。组件是页面的组成部分，每个页面功能由一个或多个组件拼凑而成。你可以通过拖拽或双击组件的方式将组件添加到当前页面。组件在页面内可以叠加多次使用，新添加的组件将自动添加在页面已有组件下方。

![组件库](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/comptents20210629.png)

组件由**组件库**和**模板库**组成。

- **组件库**分为**内置组件**和**社区组件**。
    - **内置组件**为ViCode产品自带的组件，常见的内置组件分类如下：
        - **全局组件**：你在某一页面内添加了一个全局组件，意味着整个应用内的所有页面将共享该全局组件。
        - **布局组件**：布局组件用于定义应用的布局，有助于在应用中定位组件。
        - **模块组件**：模块组件仅添加在当前页面，每个模块组件将携带一些基本配置，用于快速生成页面展示及功能。
        - **模态视图**：通常用于显示独立的内容，在模态视图显示的时候，它暂时阻断程序常规业务的执行流程，用户无法再与上一个场景交互，只能对当前此窗口进行操作。
        - **输入组件**：输入组件包括选择器、文件上传、开关等，实现人机交互。
        - **展示组件**：显示组件包括图片、文本，主要实现页面显示。
        - **图表组件**：用于显示各种图表类组件，用作可视化图表展示。
    - **社区组件**为引用的外部第三方的社区组件库，目前支持Echarts for React、React、Material-UI、React Bootstrap、Ant Design、Ant Design Charts 社区组件库的大部分组件。
- **模板库**：将已开发完成的组件发布为模板，即可在模板库中展示，以便进行再次使用。
## 添加组件

你可以选中页面，打开组件栏，拖拽组件至页面内，或双击组件，组件将自动添加至当前选中页面。

![添加组件](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/addcomptents20210608.png)

## 删除组件

在应用的编辑界面，有如下几种方式可删除组件。

>**说明：**
>
>被删除的组件无法复原，只能重新生成，请谨慎操作。

- 方式一：选中组件，单击组件导航中的“删除”图标。

    ![删除组件方式一](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/compentdelete20210425.png)

- 方式二：在大纲页面中，选中组件名称，右击选择“删除”选项。

    ![删除组件方式二](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/delete220210425.png)

- 方式三：选中组件，单击键盘上的“Delete”键。

## 复制组件

在应用的编辑界面，有如下几种方式可复制组件。

- 方式一：选中组件，单击组件导航中的“复制”图标。
  
    ![复制组件方式一](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/copycompent120210425.png)

- 方式二：在大纲页面中，选中组件名称，右击选择“复制”选项。

    ![复制组件方式二](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/copycompent220210425.png)

## 发布为模板

若需要将自定义的组件发布为模板，以便在下次使用。可以右击当前自定义的组件，选择”发布为模板“选项，进行发布。发布完成的模板在”模板库”中展示。

![发布模板](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/publishtemplate20210608.png)

>**说明：**
>
>已发布为模板的组件，在“模板库”中，右击组件可编辑组件信息、查看历史版本、删除模板库中的组件。
