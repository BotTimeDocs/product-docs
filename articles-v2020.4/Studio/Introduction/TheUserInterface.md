# 用户界面

云扩RPA编辑器采用简单直观的布局，可以最大程度地为编辑区域提供空间，同时为浏览项目或项目的整个上下文留出足够的空间。其用户界面分为以下开始主页和编辑器主页两部分：
## 开始主页 ##
![开始主界面](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/start20201019.png)

1. **新建** — 新建流程项目或组件项目。
2. **最近** — 打开您最近处理过的项目。可以打开项目所在的文件夹或从**最近使用**列表中删除；单击**更多项目**链接，展开更多的最近处理过的项目，且可模糊搜索**最近使用**列表。

### 新建 ###
![新建](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/start20201118.png)
1. **新建** — 新建流程项目或组件项目。
2. **从模板新建** — 从预定义的模板开始一个新项目。
3. **流程市场** — 在流程市场中选择并打开已有的流程的基础上进行新建项目。

### 打开 ###

![打开](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/indexopen20201118.png)

1. **最近使用** — 打开您最近处理过的项目。
2. **本地项目** — 本地电脑中已有的项目。

   - 浏览：打开本地电脑中已有的项目。
   - 刷新：重新加载当前路径下的项目文件夹。
   - 导入：导入本地电脑中已有的项目。

3. **控制台流程** — 查看/编辑控制台流程。

### 工具 ###

![工具](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/tool20201019.png)

1. **应用** — 支持**元素探测器**应用小工具。
2. **扩展** — 可以快速安装各种扩展程序，以对不同的应用进行自动化。

### 设置 ###

**设置**用于管理编辑器相关的设置信息，同时还可以找到产品的版本信息。 

* 常规 - 显示编辑器的语言配置。
* 项目 - 对项目相关信息进行设置。
   <!-- * 要更改项目存储位置，只需要在“工作目录”后更换新路径。 -->
   * “运行时最小化”让你可以将编辑器窗口设置为运行时是否最小化。
* 管理市场 - 对组件市场、代码市场、流程市场进行管理操作，包括新增、删除、启用/禁用、上移/下移等。

### 帮助 ###
**帮助**可将您定向到在线课程、产品文档、发行说明、在线资源，社区论坛和官网。还可以在**帮助**页面中找到有关产品版本等信息。
![帮助信息](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/help20201118.png)

## 编辑器主页 ##


![编辑器主界面](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/userinterface20201019.png)

1. **菜单栏** — 一种树形结构，为编辑器提供一些功能入口。
2. **工具栏** — 位于编辑器的最左侧，使你可以开展广泛的活动，包括新建、运行你的自动化项目和启动相关工具。
3. **工具面板** — 使你可以访问诸如项目、组件之类的不同面板视图，在你处理项目时为你提供帮助。
4. **编辑区域** — 作为编辑器的主要区域，使你可以编辑和修改自动化项目。
5. **输出面板** — 在编辑器下方可以打开输出面板，以输出不同的日志信息，如错误、调试等。
6. **属性栏** — 选择任一组件，在编辑器右侧可查看该组件的属性相关信息。
7. **状态栏** — 展示打开的项目和编辑器通知等相关信息。

### 项目面板 ###

**项目面板**以树形结构的方式显示你创建的全部的项目内容。 

项目面板提供一些按钮，对项目进行保存操作，来帮助你完成自动化流程的快速实现。

<!-- - **新建项目** - 创建一个新的自动化项目 -->
- **保存** - 将当前编辑好的流程保存
- **全部保存** - 将所有编辑好的流程保存
<!--- **导入项目** - 导入外部的自动化项目到编辑器里，以供使用（导入项目入口为**开始 > 打开 > 本地项目 > 导入**）-->

![项目面板](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/workindex20201019.png)

右击项目面板的任意文件或文件夹，可以打开包含以下选项的上下文菜单： 
|选项 |	描述 |
|-----------|---------------------------------------|
|打开 	|打开项目或文件| 
|添加|选择可以在所选中项目下添加的选项：[序列](../process/developProject/TypeOfWorkflow/Sequence.md)、[流程图](../process/developProject/TypeOfWorkflow/Flowchart.md)、[状态机](../../Activities/WorkflowControl/StateMachine/StateMachine.md)、文件夹|
|导入文件| 导入本地文件至当前所指定的文件夹下|
|重命名 	|使你可以重命名当前所选文件或文件夹 |
|删除 	|删除所选中的文件或文件夹 |
|导出项目 |	将所选中的项目导出，导出后会自动生成一个 .dgs(流程项目) 或 .egs（组件项目） 文件|
|引用项目|引用其他项目（支持文件夹和文件）作为依赖项|
|打开所在文件夹| 	打开所选项目或文件的本地文件夹 |
|项目设置| 	打开[项目设置](../process/ProjectSettings.md)以设置某一类别组件属性 |
|属性|查看或编辑项目的属性信息，包括项目名称、作者、版本等|
|调试文件| 	调试所选中的.xaml文件|
|运行文件| 	运行所选中的.xaml文件 |
|从项目中排除|将文件夹或文件从项目中排除，点击右上角的“显示所有”可显示排除的文件夹或文件,其中项目文件夹、依赖项、Main.xaml、project.json不支持排除|
|包括在项目中|将被排除的文件夹或文件包括到项目中,其中项目文件夹、依赖项、Main.xaml、project.json不支持排除|

>注意： 
>
>1.一个项目下面会自动创建一个主流程文件：Main.xaml，并且这个主流程文件不允许重命名
>
>2.一个项目下面可以新建任意个子流程文件（文件名任意）

### 大纲面板

**大纲面板**用于显示当前流程文件的层级结构。通过在大纲中选中某一组件来定位到编辑区域的组件，也可以通过在编辑区域选择组件来显示大纲中的组件。

![大纲面板](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/guideline20201019.png)

### 组件面板

**组件面板**主要显示自动化项目中所需要使用的组件，用鼠标拖拽到编辑区域中进行使用。组件面板提供快速查找工具的搜索框，输入组件名称即可搜索。 

通过F1快捷键或者组件右键菜单的“帮助”，可快速打开对应组件的帮助文档，以了解相应组件的详细信息及使用方法。

![组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/activitypanel20201019.png)

### 运行面板

**运行面板**主要显示与运行和调试有关的所有信息，顶部显示带有调试和运行命令的相关按钮。

**运行**自动化项目时，所有项目运行时相关过程的详细信息都将显示在输出面板中。当流程出现错误时，通过日志你可以轻松地定位到出现错误的组件。

![运行时](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/runpanel20201019.png) 

**调试**主要通过对流程设置断点，进而识别并清除流程中的错误，完善该流程并提高其正确性。当调试时，将会同时打开变量面板和输出面板，显示相关调试信息。有关调试的详细信息，请查看[调试](../process/Debugging/Debugging.md?_v=v2020.4)。

![调试](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-debug.png)

### 版本控制面板

**版本控制面板**用于记录项目中文件内容的变化，以便将来查看指定版本的修订情况。单击“启用”，开启版本控制功能。

![版本控制](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/versioncontrol20201214.png)


### 市场面板

**市场面板**使你可打开组件市场和流程市场。

* **组件市场**-使你可以下载和管理第三方的组件，将其作为依赖项添加至自动化项目中。

* **代码市场**-集成了 NuGet，使你可以更方便地加载 NuGet 包到自动化项目中。 

* **流程市场**-你可以下载流程，已完成对相关组件的了解及应用。 

有关市场的详细信息，请查看[云扩市场](../market/Market.md?_v=v2020.4)。

![市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/marketpanel20201019.png)

<!-- ![组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar.PNG)![流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar.PNG) -->

<!--### 扩展面板

**扩展面板**使你可以快速安装各种扩展程序，以对不同的应用进行自动化。

![扩展面板](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-extension.PNG)-->

### 发布项目

通过工具栏的**发布**按钮可将自动化项目打包进行发布，方便后续的执行及共享。

自动化项目发布后，将会自动存储到对应的位置，如果后续要对该位置的项目进行修改，在本地修改后，再次发布即可。

有关发布自动化项目的详细信息，请查看[发布自动化项目](../process/PublishProject.md?_v=v2020.4)。


### 个人信息

通过点击菜单栏右侧的![个人信息](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-user.PNG)打开**个人信息**退出登录。 
 
![个人信息](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-usersetting.png)


### 编辑区域 

**编辑区域**显示你正在进行的项目，你可以对其进行更改。而在编辑区域的底部导航栏能够让你快速访问变量、参数以及导入命名空间。

![设计](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/design.png)

- 通过双击某一个组件，可以查看此组件的具体内容，也可以对其进行属性的添加和更改。 

- 通过点击![移动画布](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/movethecanvas.png)图标，按住空格键或按鼠标中键来激活平移模式。

- 通过按住Ctrl+鼠标滚动方式更改缩放级别，然后点击![重置为100%](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/100%25.png)图标将其重置为100%。

- 通过点击![自适应](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/self-adaption.png)图标，使整个自动化项目按照编辑区域的大小进行自适应。



### 上下文菜单 

通过上下文菜单，你可以对当前组件进行多种操作，例如复制、粘贴、删除等。在当前组件区域点击鼠标右键即可打开上下文菜单。 

![编辑区域菜单](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/rightmenu20201215.png)



   |选项         |描述|
   |----------------|---------------------------------------|
   |打开         |打开编辑区域中选中的组件，也可以通过双击来实现。|
   |剪切         |删除选中的组件并将其放在剪贴板上。|
   |复制         |复制选中的组件并将其放在剪贴板上。|
   |粘贴         |将剪贴板上的组件插入到当前位置。|
   |删除         |删除选中的组件。|
   |批注         |对组件进行注释的添加、编辑、删除、显示和隐藏。|
   |断点         |对选定的组件进行断点的插入、删除、禁用和启用。|
   |包括在错误捕获中|将选择的单个组件用错误捕获组件包括起来，包括在Try模块中。|
   |创建变量      |在变量列表中创建变量。|
   |提取为子流程   |创建一个包含目标组件的新流程。通过将大型流程拆解，以降低查看项目的复杂度。</br>在提取为子流程的组件处会自动生成一个调用流程组件，参数由组件中使用的变量自动生成。|
   |启用组件 |启用先前禁用的组件。|
   |禁用组件 |禁用选定的组件，并将其放置在**注释掉**容器中|
   |导出到Excel |鼠标右击容器内组件（流程图/序列/状态机组）的空白处，将 xaml 文件内容导出到 Excel 中。|
   |复制为图像    |将编辑区域中显示的内容保存为图片，图片名称、类型、存储路径等为默认状态。|
   |另存为图像    |将编辑区域中显示的内容保存为图片，但图片的名称、类型、存储路径等可以进行自定义。|
   |显示所有条件|在流程编辑区域将流程决策组件的条件（Condition）属性值显示出来。|
   |隐藏所有条件|在流程编辑区域将流程决策组件的条件（Condition）属性值隐藏起来。 |
   |帮助 |快速打开对应组件的帮助文档，以了解相应组件的详细信息及使用方法，也可以通过快捷键F1实现。|
   |设置为开始节点 |将当前选中组件设为开始节点，流程执行由当前组件开始。 </br> 注意：只在当前容器组件为流程图时显示。|
   |查看父级     |在编辑区域中显示当前选中组件的父级。 </br> 注意：只在子级组件的上下文菜单中显示。|


### 属性面板

**属性面板**在编辑区域内部呈现，其显示当前组件的相关属性，你可以通过属性面板对当前组件的属性进行相关设置。 

>注意： 
> 
>输入属性值时，若属性值为字符串，需要将字符串放在英文双引号中。 

![属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/properties.png)

### 输出面板

**输出面板**可以显示当前项目中的所有信息，包括但不限于项目打开或执行时的信息、写入日志组件的输出信息。通过输出面板，你可以快速定位到项目中错误出现的位置，及时更改，保证项目的正确性。

在输出面板中，可以t通过点击面板标题栏的不同按钮来显示或隐藏不同日志级别的消息，例如错误、信息、调试。右键单击消息，将会把该消息复制到粘贴板中。

当项目验证出现问题时，将在输出面板中显示错误信息。针对调试项目时，输出面板将显示所有组件从开始到结束的详细日志。当流程出错，通过日志信息将可以轻松地定位到出现错误的组件。

请注意，每次运行或调试项目时，将会自动清除此面板中存储的日志信息。

![属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/outputPanel.png)

## 意见反馈

**意见反馈**可以使你快速地寻求帮助。通过点击![在线咨询](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/help.png)图标，打开反馈窗口。

当我们的客服人员在线时，你可以将你的问题反馈给客服人员，客服人员将会及时帮助你解决问题；当客服人员不在线时，你也可以通过留言来反馈你的问题。