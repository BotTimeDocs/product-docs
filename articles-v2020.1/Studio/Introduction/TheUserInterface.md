# 用户界面
云扩RPA编辑器的用户界面主要由工具栏、工具窗口以及设计窗口三个区域组成。 

![编辑器主界面](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/mainInterface.PNG)

1、**工具栏** — 使你可以开展广泛的活动，包括保存、运行你的自动化流程和启动相关工具。

2、**工具窗口** — 使你可以访问特定任务，如工作目录、组件、属性等。你可以展开它们或折叠它们。 

3、**设计窗口** — 使你可以编辑和修改自动化流程项目。 

## 工具栏
工具栏包含开始、设计、调试、扩展、帮助和个人设置。
![工具栏](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar.PNG)

### 开始 

**开始**使你可以新建一个项目或直接打开近期处理的项目。 
 
**设置**用于切换工作目录和设置默认语言。默认情况下，语言为简体中文。 

> 注意：
> 
>切换工作目录前需要保证当前所有的项目已保存。 
 
![开始](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/start.png)

### 设计
**设计**使你可以对项目进行各种操作，包括新建、保存及运行等。你还可以使用相关工具来帮助你完成自动化流程的快速实现，比如录制、组件市场及流程市场。 

* **录制**-通过录制器可以完成对网站应用程序、桌面应用程序的自动化操作。 
* **组件市场**-使你可以下载和管理第三方的组件，将其作为依赖项添加至自动化项目中。 
* **流程市场**-你可以下载流程，已完成对相关组件的了解及应用。 

![设计](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-design.PNG)

### 调试
**调试**主要通过对流程设置断点，进而识别并清除流程中的错误，完善该流程并提高其正确性。有关调试的具体信息，请查看[调试](../Debugging.md)。

### 扩展 
**扩展**使你可以快速安装Java扩展。

![扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-extension.PNG)
 
### 帮助 
**帮助**使你能够快速打开产品文档、在线课程、社区论坛。 
你还可以通过帮助中的“联系我们”，向我们发送一些意见或建议。也可以在“关于我们”中了解到产品的版本信息。 

![帮助](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-help.PNG)

 
### 个人设置 
点击编辑器界面右上角的![个人设置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-user.PNG)打开上下文菜单进行用户注销。 
 
![个人设置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-usersetting.png)

## 工具窗口 
**工具窗口**主要包括工作目录窗口、组件窗口、日志窗口以及属性窗口四个模块。 

### 工作目录窗口 
**工作目录窗口**以树形结构的方式显示你创建的全部的项目内容，你可以通过双击项目名打开该项目。 
 
点击“刷新”图标可以重新加载工作目录，点击“新建文件”图标可以为当前项目添加一个子流程。

![工作目录](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/workspace.PNG)

右击工作目录窗口的任意文件或文件夹，可以打开包含以下选项的上下文菜单： 
|选项 |	描述 |
|-----------|---------------------------------------|
|打开 	|打开项目或文件| 
|新增文件|在所选中项目下添加子流程。</br>注意：仅在选择项目时出现 |
|重命名 	|使你可以重命名当前所选文件或文件夹 |
|删除 	|删除所选中的文件或文件夹 |
|导出项目 |	将所选中的项目导出，导出后会自动生成一个 .dgs 文件</br>注意：仅在选择项目时出现 |
|打开所在文件夹| 	打开所选项目或文件的本地文件夹 |

>注意： 
>
>1.一个项目下面会自动创建一个主流程文件：Main.xaml，并且这个主流程文件不允许重命名。 
>
>2.一个项目下面可以新建任意个子流程文件（文件名任意）

### 组件窗口 
**组件窗口**主要显示项目中所需要使用的组件，用鼠标拖拽到设计窗口中进行使用。组件窗口提供快速查找工具的搜索框，输入组件名称即可搜索。 

筛选按钮点击后是一个列表，其中包含几个组件显示选项：最近使用、我的收藏、可用的、扩展。勾选后，将会使对应的选项下的组件始终可见。 
 
![组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/activities.png)

### 日志窗口 
**日志窗口**主要是显示项目运行时相关过程的详细信息，你可以从这里获取项目运行的过程信息，便于定位项目出错的位置。 
 
![日志](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/logs.PNG)
 
### 属性窗口 
**属性窗口**显示当前组件的相关属性，你可以通过属性窗口对当前组件的属性进行相关设置。 

属性窗口提供两种排序方式，一种是按照分类排序，一种是按照字母排序。它还提供搜索框对属性进行快速查找。 
 
>注意： 
> 
>输入属性值时，若属性值为字符串，需要将字符串放在英文双引号中。 

![属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/properties.png)
 
## 设计窗口 
设计窗口可以显示你正在进行的项目，你可以对其进行更改。而在设计窗口的底部导航栏能够让你快速访问变量、参数以及导入命名空间。

通过双击某一个组件，可以查看此组件的具体内容，也可以对其进行属性的添加和更改。 
 
![设计](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/design.png)
 
### 上下文菜单 
通过上下文菜单，你可以对当前组件进行多种操作，例如复制、粘贴、删除等。在当前组件区域点击鼠标右键即可打开上下文菜单。 

![设计窗口菜单](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/design-menu.png)


   |选项         |描述|
   |----------------|---------------------------------------|
   |打开         |打开设计窗口中选中的组件，也可以通过双击来实现。|
   |查看父级     |在设计窗口中显示当前选中组件的父级。 </br> 注意：只在子级组件的上下文菜单中显示。|
   |剪切         |删除选中的组件并将其放在剪贴板上。|
   |复制         |复制选中的组件并将其放在剪贴板上。|
   |粘贴         |将剪贴板上的组件插入到当前位置。|
   |删除         |删除选中的组件。|
   |批注         |对组件进行注释的添加、编辑、删除、显示和隐藏。|
   |断点         |对选定的组件进行断点的插入、删除、禁用和启用。|
   |复制为图像    |将设计窗口中显示的内容保存为图片，图片名称、类型、存储路径等为默认状态。|
   |另存为图像    |将设计窗口中显示的内容保存为图片，但图片的名称、类型、存储路径等可以进行自定义。|
   |创建变量      |在变量面板中创建变量。|
   |提取为子流程   |创建一个包含目标组件的新流程。通过将大型流程拆解，以降低查看项目的复杂度。</br>在提取为子流程的组件处会自动生成一个调用流程组件，参数由组件中使用的变量自动生成。|
   |设置为开始节点 |将当前选中组件设为开始节点，流程执行由当前组件开始。|
