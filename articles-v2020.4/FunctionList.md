# 云扩产品功能清单

## 编辑器

### 功能点列表


1. 新增[新建组件项目](./Studio/process/CreateLibrary.md)，将多个可重复使用的流程封装为组件包，可发布到组件市场供其它项目使用。
2. 新增[从模板新建自动化项目](./Studio/process/ProjectTemplates.md),支持 RPA 实施人员规范 RPA 流程开发方式，提升企业级的 RPA 流程实施质量。
3. 支持查看和编辑当前登录用户在控制台所属资源组下的流程。
4. 新增项目右击操作（打开文件夹/项目设置/添加状态机文件）。
5. 调试状态下，当发生错误时，支持忽略、重试、重启操作。
6. 当光标置于任意输入框时，支持快捷键**Ctrl+E**快速打开表达式编辑器。
7. 新增**开始菜单页**Homepage视图，拆分项目编辑和非编辑操作页面，降低项目编辑过程中的干扰率，提升流程编辑效率。
8. 新增Microsoft Edge浏览器扩展插件，在进行自动化 Edge 操作之前，请先安装 [Microsoft Edge 扩展](Studio\Extensions\EdgeExtension.md)。
9. **选择器编辑器**新增获取 XPath 功能，可以使用 XPath 的形式对元素进行展现，参见[选择器](Activities\Appendix\Selector.md)。
10. 新增 **IE 前端日志收集器**应用程序，使用该应用程序调试用 IE 完成的 RPA 流程并获取调试日志，参见[收集 IE 前端日志工具](Activities\Appendix\IELog.md)。
11. 支持**大纲**层级显示，用于显示当前流程的结构，可快速定位对应组件。
12. 当光标置于属性输入框内时，鼠标右键可快速打开**表达式编辑器**菜单，对变量、参数或表达式进行操作。
13. 新增全局快捷键 **Ctrl+Alt+F5**，使编辑器最小化后在后台运行时,也能够停止执行流程。
14. 暂停调试支持在任意时刻快速暂停调试过程。暂停时，正在调试的组件将高亮显示。
15. 流程编辑过程中，通过右键组件可选择禁用或启用组件。运行或调试时，禁用的组件将会被忽略执行。
16. 在主界面菜单栏中新增**意见反馈**按钮，可快速寻求帮助。
17. 输出面板支持分类筛选输出信息，包括**错误**、**信息**、**调试**这三类，用于分类查看日志信息。
18. 支持在表达式编辑器中，选中变量名，使用 **Ctrl+B** 快捷键快速创建变量。
19. 针对含有多个xaml文件的复杂流程，支持通过[调试/运行文件](Studio\process\Debugging\partialDebug.md)来进行分布调试。
20. 支持使用编辑器直接发布自动化项目到本地机器人,实现无缝对接。
21. 在编辑器右下角支持浮窗通知，针对编辑器更新、部分项目操作反馈进行提醒，降低了弹窗通知带来的干扰率，提升用户体验。
22. 集成 NuGet 开源项目，可以方便的引用 NuGet 应用。
23. 支持使用元素探测器选择元素，功能较此前的选择器编辑器更强，此功能仅在企业版中支持，可参见[元素探测器](Activities/Appendix/UiDetector.md)。
24. 在项目设置中，支持设置组件的延迟和超时属性，支持配置默认浏览器属性，可参见[项目设置](Studio/process/ProjectSettings.md)。
25. 调试过程中，支持在[变量面板](Studio\process\Debugging\ValuePanel.md)查看每一个变量在当前组件的类型和值，以此我们可以来判断流程是否正确执行，且可帮助定位流程错误位置。
26. 新建项目时，支持根据当前录制的桌面应用选择对应录制技术：UIA3或UIA。
27. 在导入列表处，支持删除未使用或报错的[命名空间](Studio\process\developProject\ImportNamespaces.md)。
28. 项目运行时，支持最小化编辑器主界面，降低对界面自动化项目运行的干扰率。
29. 支持更多的快捷键，参见[键盘快捷键](Studio/quickStart/KeyboardShortcuts.md)，使用户使用更便捷。
30. 支持一种360安全浏览器类型。
31. 支持将流程中的组件保存为子流程文件，你可以使用本功能将复杂流程拆解为多个简单的流程。

### 改进与增强

1. 在**开始菜单页**中优化调整**流程市场**、**组件市场**等应用的入口位置。
2. 更换安装框架，优化安装/升级体验，解决了由杀毒软件导致的安装失败问题。
3. 非管理员权限运行编辑器时，元素识别时高亮外层窗体，并在点击时提示。
4. 选择器编辑器中Java应用的Name属性全部层级支持通配符。
5. 选择器编辑器界面优化，使得用户操作体验更友好。
6. 界面自动化组件支持即刻优雅终止流程。
7. 优化项目打开速度，较之前更快，提升用户体验。
8. 优化复制粘贴组件速度，较之前更快，提升用户体验。
9. 项目运行或调试过程中，输出面板对当前过程进行提示，使用户更加明确当前执行过程。
10. 发布项目前，对项目的正确性进行校验。
11. 将部分弹窗更改为浮窗，提升用户体验。
12. 支持新增序列或流程图作为子流程。
13. 导出项目时，支持导出后选择是否打开所在文件夹。
14. 导入项目时，支持导入后选择是否立即打开该项目。
15. 统一项目名称及流程包名称的命名规则，避免发布流程时名称校验不通过。
16. 支持 Java 扩展。你可以使用 Java 扩展识别一些原本无法识别的桌面 Java 应用中的元素。
17. 日志输出界面优化，由左侧显示更改为编辑器底部显示，使之更全局化，提升用户体验。
18. 支持更详细的项目打开及编译错误描述，更易定位错误位置。
19. 增强**表达式编辑器**的**智能感知**功能，支持变量/参数/方法名称联想。
20. 针对社区版许可证超出配额的情况，增加解决方法的提示。
21. 在创建变量/参数时，支持快速创建 DataTable / IUiObject 类型的变量/参数。
22. 支持通过组件的右键菜单来访问组件的帮助文档。

### 问题修复

1. 修复了表达式编辑时，自动补入变量名不齐全的问题。
2. 修复了调试时不能查看容器类组件中最后一个组件的属性的问题。
3. 修复了搜索组件时，搜索结果展示不全的问题。
4. 修复了修改变量值后，调试项目时，修改不生效的问题。
5. 修复了编辑器界面偶尔无法点击的问题。

## 组件

### 功能点列表

1.  **软件自动化 > PDF**：[合并文件](Activities/AppAutomation/PDF/MergePDF.md)、[提取为新文档](Activities/AppAutomation/PDF/ExtractToNewFile.md)、[获取页数](Activities/AppAutomation/PDF/GetPageNumbers.md)、[读取图片](Activities/AppAutomation/PDF/ExtractImages.md)、[读取文本](Activities/AppAutomation/PDF/ExtractText.md)
2.  **系统 > 文件 > [重命名文件或文件夹](Activities/System/File/RenameFileOrFolder.md)**
3. **系统 > [输入密码](Activities/System/InputPasswordDialogActivity.md)**
4. **控制台 > [文档理解](Activities/Console/DocReader.md)**：内置文档理解组件，只要控制台部署了文档理解服务，就可以使用文档理解的功能。
5. **控制台 > [获取资产](Activities/Console/GetAssets.md)**：可以直接在流程中，使用 获取资产组件，获取在控制台保存的数据资产。
5.  **代码工具 > 数组处理**：[初始化数组](Activities/CodeExecuter/数组处理/InitializeArrayActivity.md)、[元素是否存在](Activities/CodeExecuter/数组处理/ExistsInArrayActivity.md)、[获取数组长度](Activities/CodeExecuter/数组处理/GetLengthOfArrayActivity.md)
6.  **代码工具 > HTTP > [下载文件**
8.  **(Activities/CodeExecuter/HTTP/HTTPDownload.md)**

1. **触发器 > [文件触发器](Activities/Triggers/FileTrigger.md)**：用于监听指定文件夹下文件变化，设置特定触发条件并自动执行流程。
2. **触发器 > [邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md)**：用于监听 Outlook 邮箱接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。
3. **触发器 > [邮件触发器(Exchange)](Activities/Triggers/ExchangeTrigger.md)**：用于监听 Exchange 服务器接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。
4. **触发器 > [邮件触发器(IMAP)](Activities/Triggers/IMAPTrigger.md)**：用于监听支持 IMAP 协议的邮箱接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。
5. **代码工具 > JSON > [序列化](Activities/CodeExecuter/JSON/SerializeObject.md)**：可将.NET对象序列化为 JSON 字符串。
6. **代码工具 > JSON > [反序列化](Activities/CodeExecuter/JSON/DeserializeObject.md)**：可将 JSON 字符串反序列化为.NET对象。
7. **软件自动化 > Office Excel > [刷新透视表](Activities/AppAutomation/OfficeExcel/RefreshPivotTable.md)**：实现刷新指定透视表的数据。
8. **软件自动化 > Office Excel > [创建透视表](Activities/AppAutomation/OfficeExcel/CreatePivotTable.md)**：实现在 Excel 中创建透视表。
9. **代码工具 > HTTP > [HTTP请求](Activities/CodeExecuter/HTTP/HTTPRequest.md)**：实现发送 HTTP 请求并返回响应的数据，并支持测试配置的 HTTP 请求是否可用。

1. **系统 > [提示框](Activities/System/PromptBox.md)**：用于在Windows桌面右下角展示在流程中必要的提示信息。
2. **软件自动化 > Office Excel > [ 重置密码](Activities/AppAutomation/OfficeExcel/OfficeExcelResetPassword.md)**：在**打开/新建**组件中使用，对 Excel 文件进行增加、更新或清除密码。

1. **界面自动化 > [匹配图片](Activities/UIAutomation/MatchImage.md)**：实现在指定范围内寻找指定图片，返回符合的结果集。
2. **界面自动化 > [设置焦点](Activities/UIAutomation/SetFocus.md)**：实现为指定元素设置焦点，支持桌面端和浏览器端。
3. **界面自动化 > [选择多个项目](Activities/UIAutomation/SelectMultipleItems.md)**：实现多个项目的同时选择，此组件仅当原页面支持多选时生效。
4. **界面自动化 > [高亮](Activities/UIAutomation/Highlight.md)**：实现指定元素高亮，可选择颜色和时间。
5. **界面自动化 > [等待元素属性值](Activities/UIAutomation/WaitElementAttributeValue.md)**：实现等待指定元素的属性值为指定值时，才执行下一个组件，否则会在超时时间范围内一直等待。
6. **界面自动化 > [获取元素属性值](Activities/UIAutomation/GetElementAttributeValue.md)**：实现获取指定元素的属性值，并将其存储在输出变量属性值中。
7. **界面自动化 > OCR > [获取 OCR 文本](Activities/UIAutomation/OCR/GetOCRText.md)（企业版）**：实现对指定元素或图片进行 OCR 并返回结果。
8. **界面自动化 > OCR > [获取含 OCR 文本的元素](Activities/UIAutomation/OCR/GetSpecificTextOCRElement.md)（企业版）**:实现对指定元素或图片进行OCR，并查找包含指定文本的元素，将其存储在输出属性 OCR 元素内。
9. **界面自动化 > OCR > [判断 OCR 文本是否存在](Activities/UIAutomation/OCR/IdentifyOCRTextExist.md)（企业版）**：实现对指定元素或图片进行 OCR ，并判断指定文本是否存在，将其结果存储在输出属性 OCR 元素内。
10. **软件自动化 > 邮件**：[获取邮件(Exchange)](Activities/AppAutomation/Mail/GetExchangeMail.md) 、 [发送邮件(Exchange)](Activities/AppAutomation/Mail/SendExchangeMail.md)
11. **代码工具 > 文本处理**: [验证文本有效性](Activities/CodeExecuter/TextProcessing/VerifyTextActivity.md)、[提取文本](Activities/CodeExecuter/TextProcessing/ExtractTextActivity.md)、 [替换文本](Activities/CodeExecuter/TextProcessing/ReplaceTextActivity.md)、[截取文本](Activities/CodeExecuter/TextProcessing/GetSubstringActivity.md)、[获取文本长度](Activities/CodeExecuter/TextProcessing/GetLengthOfTextActivity.md)、[获取文本索引](Activities/CodeExecuter/TextProcessing/GetIndexOfTextActivity.md)
12. **流程控制 > [赋值（多个） ](Activities/WorkflowControl/MultipleAssign.md)**
13. **软件自动化 > Office Excel > [插入图片](Activities/AppAutomation/OfficeExcel/InsertPicture.md)**：实现指定单元格插入图片。
14. **流程控制 > 判断 > [条件(Switch)](Activities/WorkflowControl/Determine/Switch.md)**：实现指定C#表达式，并根据每个Case判断执行符合条件的流程。
15. **系统 > 文件 > [遍历文件夹](Activities/System/File/ForeachFolder.md)**
16. **代码工具 > 集合处理** ：[对象是否存在](Activities/CodeExecuter/CollectionProcessing/ExistsInCollectionActivity.md)、[添加对象](Activities/CodeExecuter/CollectionProcessing/AddToCollectionActivity.md)、[清空对象](Activities/CodeExecuter/CollectionProcessing/ClearCollectionActivity.md)、[移除对象](Activities/CodeExecuter/CollectionProcessing/RemoveFromCollectionActivity.md)、[获取集合长度](Activities/CodeExecuter/CollectionProcessing/GetLengthOfCollectionActivity.md)、[初始化集合](Activities/CodeExecuter/CollectionProcessing/InitializeCollectionActivity.md)

1. **流程控制 > [状态机](Activities/WorkflowControl/StateMachine/StateMachine.md)**：实现基于状态机范例的工作流程。
2. **代码工具 > 数据处理 > [数据格式化](Activities/CodeExecuter/DataProcessing/FormatData.md)**：可实现对输入数据按照数值、日期和时间、货币和百分比进行格式化。
3. **流程控制**：[重试](Activities/WorkflowControl/Retry.md)、[抛出异常](Activities/WorkflowControl/Throw.md)、[重新抛出异常](Activities/WorkflowControl/ReThrow.md)。
4. **系统 > [下拉选择框](Activities/System/DropdownListDialog.md)**：方便在流程中弹出下拉选择框形态的用户交互界面。
5. **数据表 > [追加到CSV文件](Activities/DataTable/AppendToCSV.md)**：实现将数据表追加到已有CSV文件。
6. **软件自动化 > 邮件**：[获取邮件(Outlook)](Activities/AppAutomation/Mail/GetOutlookMail.md)、[发送邮件(Outlook)](Activities/AppAutomation/Mail/SendOutlookMail.md)。
7. **界面自动化 > 桌面控件专有**：[获取焦点控件](Activities/UIAutomation/DesktopOnly/GetFocus.md)、[切换控件](Activities/UIAutomation/DesktopOnly/SwitchControl.md)，这两个控件仅在企业版中支持。

1. **界面自动化 > SAP** ：[登录应用](Activities/UIAutomation/SAP/SAP_Login.md)、[获取状态栏信息](Activities/UIAutomation/SAP/SAP_GetStatus.md)、[选择日期](Activities/UIAutomation/SAP/SAP_SelectCalendar.md)、[选择SAP项](Activities/UIAutomation/SAP/SAP_Select.md)、[执行事务](Activities/UIAutomation/SAP/SAP_Transaction.md)，仅在企业版中支持这些组件。
2. **界面自动化 > [截屏](Activities/UIAutomation/Screenshot.md)**。
3. **系统 > [设置日期和时间](Activities/System/SetDateTime.md)**：实现指定日期和时间并输出DateTime类型结果。
4. **系统**：[选择文件](Activities/System/File/SelectFile.md)、[选择文件夹](Activities/System/File/SelectFolder.md)。
5. **软件自动化 > Office Excel > [设置文字颜色](Activities/AppAutomation/OfficeExcel/SetTextColor.md)** ：使用拾色器提升颜色设置体验。

1. **软件自动化 > 邮件 > [获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md?_v=v2020.4)**。
2. **软件自动化 > Office Excel > [自动填充](Activities/AppAutomation/OfficeExcel/AutoFillRange.md?_v=v2020.4)**。
3. **系统 > [设置剪贴板文本](Activities/System/SetContentsToClipboard.md?_v=v2020.4)**：实现设置文本内容到剪贴板。
4. 在**组件市场**中新增[Office PowerPoint组件包](https://marketplace.encoo.com/#/activity/detail?packageId=Encootech.OfficePPT)，实现对PPT常用功能的支持。
5. 在**组件市场**中新增[竹间智能语音识别](https://marketplace.encoo.com/#/activity/detail?packageId=Emotibot)，实现语音转文字功能 。

### 改进与增强

1. **触发器 > [文件触发器](Activities/Triggers/FileTrigger.md)**： 增加输出监听的文件路径。
2. **触发器 > 邮件触发器**：[邮件触发器(IMAP)](Activities/Triggers/IMAPTrigger.md)、[邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md)和[邮件触发器(Exchange)](Activities/Triggers/ExchangeTrigger.md) 增加输出监听到的新邮件。
3. **软件自动化 > Office Excel > [获取末列号](Activities/AppAutomation/OfficeExcel/GetLastColumn.md)**：增加输出字母和数字列号。

1. 界面自动化下的组件全部新增超时属性。
2. **获取含OCR文本的元素**、**判断OCR文本是否存在**组件的文本属性支持正则表达式。
3. 优化钉钉程序内元素识别，使得录制技术 UIA 可识别大部分元素。

4. 提升[调用流程](Activities/WorkflowControl/InvokeWorkflow.md)组件体验，点击**导入参数**可直接将子流程参数导入。

1. [发送邮件(SMTP)](Activities/AppAutomation/Mail/SendMailSMTP.md)、[获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md)、[获取邮件(POP3)](Activities/AppAutomation/Mail/GetMailPOP3.md)组件支持手动选择安全方式。
2. [获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md)组件支持仅获取未读邮件。

1. 优化**软件自动化 > Office Excel > [排序](Activities/AppAutomation/OfficeExcel/Sort.md)** 组件,支持指定开始行号。
2. 优化**软件自动化 > Office Excel > [设置单元格背景色](Activities/AppAutomation/OfficeExcel/SetCellBackcolor.md)** 组件,使用拾色器提升颜色设置体验。

3. 提升 **软件自动化 > Office Excel** 系列组件执行性能。

1. 加强对用友 NC 系列软件的支持。
2. 支持在金蝶 EAS 系列软件中，对报表类型界面通过**获取结构化数据**获取报表数据。
3. 在图像识别模式下，**等待元素出现**组件返回的控件元素为图象，而非锚点。
4. 支持内嵌IE浏览器中元素的识别。
5. 支持360安全浏览器兼容模式下元素的识别。
6. 浏览器端支持**图像识别**功能。
7. 对于桌面应用，**输入文本**组件支持**清空文本**操作。
8. **获取区域文本**组件更名为 **获取区域结构**（企业版）。
9. **悬停**组件支持图像识别。

1. 增强对用友 NC 系列软件和金蝶 EAS 系列软件的支持。
2. 增强桌面录制技术 UIA3 识别微信，实现获取文本、选择项目时可以自动滚动联系人列表操作。
3. 增强 JAVA 应用在不同分辨率 DPI 下的识别回放。
4. **点击**组件新增辅助键属性。如，你可以在点击的同时按下 **Ctrl** 键。



## 机器人

### 功能点列表

1. 新增[定时任务](Robot/CronJob.md)功能，使得原本需要采购控制台完成的功能，在机器人中便可完成。
1. 支持获取并运行[云扩流程市场](Robot/ProcessMarket.md)中的流程。

1. 在**设置**页面中新增[关于页](Robot/Settings/About.md)，可查看软件版本、许可证有效期及更改激活方式。
2. 新增[正在执行](Robot/RunningProcess.md)页面，可以查看正在执行的流程相关信息。
3. 在执行流程时，支持权限配置。具体功能请参见[流程库](Robot/localworkflow.md)。

1. 新增机器人[概览页](Robot/Overview.md)，可展示当前机器人全局数据。
1. 新增[流程执行历史页](Robot/ProcessHistory.md)，可展示流程执行的历史记录。
1. 新增**设置 > 基本**页面，可[配置日志与视频文件保留时间](Robot/Settings/Basic.md)。

4. 执行本地流程时支持填写流程参数，详见[执行本地流程](Robot/localworkflow.md)。



## 工作台
### 功能点列表

1. 新增顶部导航、左侧导航组件，支持应用内多页面跳转。
2. 新增流程组件，支持一键启动控制台流程。
3. 支持应用版本管理，控制台统一对应用进行上下架及版本管理。
4. 支持**我的应用**查找并运行。

## 控制台

### 功能点列表

1. 支持与工作台进行通信，在控制台中可查看已发布的应用。 
   
2. 整体架构升级，上线云端版和私有化版，支持功能包括 [调度队列](Console/queue/aboutqueue.md)、[任务记录](Console/job/aboutJob.md)、 文档理解、[资产管理](Console/asset/AboutAsset.md)。
