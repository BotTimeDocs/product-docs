# 云扩 RPA 功能清单

## 编辑器

![编辑器功能](https://docimages.blob.core.chinacloudapi.cn/images/studio.png)

### 功能点列表

**1.【项目管理】**

- 新增 [新建组件项目](./Studio/process/CreateLibrary.md)，将多个可重复使用的流程封装为组件包，可发布到组件市场供其它项目使用。
- 新增 [从模板新建自动化项目](./Studio/process/ProjectTemplates.md)，支持 RPA 实施人员规范 RPA 流程开发方式，提升企业级的 RPA 流程实施质量。
- 新增支持查看和编辑当前登录用户在控制台所属资源组下的流程。
- 在项目设置中，新增支持设置组件的延迟和超时属性，支持配置默认浏览器属性，可参见 [项目设置](Studio/process/ProjectSettings.md)。
- 新建项目时，支持根据当前录制的桌面应用选择对应录制技术：[UIA3/UIA](https://docs.microsoft.com/zh-cn/dotnet/framework/ui-automation/ui-automation-overview) 。
- 在“开始 > 打开 > 本地项目”列表上方，新增“刷新”按钮，可手动刷新本地项目列表，实现重新加载当前路径下的项目文件夹。
- 在“新建 > 从模板新建”列表中，新增“[企业流程模板](Studio/process/ProjectTemplates.md)”，可使用该模板新建标准流程。
- 支持 [引用外部项目](Studio/process/ReferenceProject.md) 作为依赖项，供当前流程使用。
- 支持启用 [版本控制（预览）](Studio/VersionControl.md) 功能：用于记录本地项目中文件内容的变化，以便将来查看指定版本的修订情况。
- 支持导入文件：将其他文件导入到当前所选文件夹下。
- 新增[清理屏幕截图](./Studio/Introduction/TheUserInterface.md)，支持清理项目中未使用到的屏幕截图，减少因截图过多而占用相当大的存储空间。
- 新增项目刷新操作，支持刷新当前项目下文件的状态。
- 支持在开始主页中导出项目和删除项目，以便更好地管理与分享项目。

**2.【开放市场】**

- 新增 [代码市场](Studio\market\NuGetMarket.md)，集成 [NuGet](https://docs.microsoft.com/zh-cn/nuget/what-is-nuget) 开源项目，可以方便的引用 NuGet 应用。
- 在 **组件市场** 中，新增 [ Office PowerPoint 组件包](https://marketplace.encoo.com/#/activity/detail?packageId=Encootech.OfficePPT)，实现对 PPT 常用功能的支持。
- 在 **组件市场** 中，新增 [竹间智能语音识别](https://marketplace.encoo.com/#/activity/detail?packageId=Emotibot)，实现语音转文字功能。

**3.【辅助工具】**

- 新增 Microsoft Edge 浏览器扩展插件，在进行自动化 Edge 操作之前，请先安装 [Microsoft Edge 扩展](Studio\Extensions\EdgeExtension.md)。
- 选择器编辑器：新增获取 [XPath](https://www.w3school.com.cn/xpath/xpath_intro.asp) 功能，可以使用 XPath 的形式对元素进行展现，参见 [选择器](Activities\Appendix\Selector.md)。
- 新增 **IE 前端日志收集器** 应用程序：使用该应用程序调试用 IE 完成的 RPA 流程并获取调试日志，参见 [收集 IE 前端日志工具](Activities\Appendix\IELog.md)。
- 新增支持使用元素探测器选择元素：功能较此前的选择器编辑器更强，可参见 [元素探测器](Activities/Appendix/UiDetector.md)。
- 企业版支持[Citrix](./Studio/Extensions/Citrix.md)，使您在 Citrix Desktop 或 Citrix App上得到和原生自动化方式一样的体验，而无需使用图像识别等自动化技术。
- 新增[选择器管理器](./Activities/Appendix/SelectorManager.md) ，用于管理带有“控件元素”或“选择器”属性的组件中的指定元素。

**4.【系统设置】**

- 项目运行时，支持最小化编辑器主界面，降低对界面自动化项目运行的干扰率。
- 在“开始 > 帮助”页面，新增 AI HUB 实用链接，方便用户更好地了解 AI HUB 产品。
- 支持切换 [激活](Studio/quickStart/Activation.md) 方式：在关于页面实现社区版/企业版编辑器激活方式的切换以便重新激活。

**5.【可视化编辑器】**

-  新增 **开始菜单页** Homepage 视图，拆分项目编辑和非编辑操作页面，降低项目编辑过程中的干扰率，提升流程编辑效率。
- 在主界面菜单栏中，新增 **在线咨询** 按钮，可快速寻求帮助。
- 在编辑器右下角支持浮窗通知，针对编辑器更新、部分项目操作反馈进行提醒，降低了弹窗通知带来的干扰率，提升用户体验。
- 新增项目右击操作（打开文件夹/项目设置/添加状态机文件）。
- 当光标置于任意输入框时，支持快捷键 **Ctrl+E** 快速打开表达式编辑器。
- 支持 **大纲** 层级显示，用于显示当前流程的结构，可快速定位对应组件。
-  当光标置于属性输入框内时，鼠标右键可快速打开 **表达式编辑器** 菜单，对变量、参数或表达式进行操作。
- 流程编辑过程中，通过右键组件可选择禁用或启用组件。运行或调试时，禁用的组件将会被忽略执行。
- 支持在表达式编辑器中，选中变量名，使用 **Ctrl+B** 快捷键快速创建变量。
- 支持使用编辑器直接发布自动化项目到本地机器人，实现无缝对接。
- 在导入列表处，支持删除未使用或报错的 [命名空间](Studio\process\developProject\ImportNamespaces.md)。
- 支持将流程中的组件保存为子流程文件，你可以使用本功能将复杂流程拆解为多个简单的流程。
- 支持更多的快捷键，参见 [键盘快捷键](Studio/quickStart/KeyboardShortcuts.md)，使用户使用更便捷。
- 调试状态下，当发生错误时，支持忽略、重试、重启操作。
-  新增全局快捷键 **Ctrl+Alt+F5**，使编辑器最小化后在后台运行时，也能够停止执行流程。
- 暂停调试支持在任意时刻快速暂停调试过程。暂停时，正在调试的组件将高亮显示。
- 输出面板支持分类筛选输出信息，包括 **错误**、**信息**、**调试** 这三类，用于分类查看日志信息。
- 针对含有多个 xaml 文件的复杂流程，支持通过 [调试/运行文件](Studio\process\Debugging\partialDebug.md) 来进行分布调试。 
- 调试过程中，支持在 [变量面板](Studio\process\Debugging\ValuePanel.md) 查看每一个变量在当前组件的类型和值，以此我们可以来判断流程是否正确执行，且可帮助定位流程错误位置。
- 支持流程 [导出到 EXCEL](Studio/Introduction/TheUserInterface.md) ：鼠标右击在流程编辑区域中容器内组件（流程图/序列/状态机）的空白处，在弹出的上下文菜单中，选择“导出到 EXCEL”，实现将 XAML 文件内容导出到 Excel 中。
- 支持单个组件包括在错误捕获中：将选择的单个组件用错误捕获组件包括在 Try 模块中，方便调试。
- 支持[搜索](./Studio/quickStart/KeyboardShortcuts.md)当前流程文件中的组件，以快速定位到该组件。
- 新增[快速访问页](./Studio/Introduction/TheUserInterface.md)，可快速打开流程文件、快速进行录制和调试、快速打开实用链接。
- 支持从选定组件开始调试流程，方便实施人员快速排查定位异常问题，提升实施人员开发效率。
- 支持快速搜索当前流程文件中的变量并定位，提升实施人员开发效率。
- 支持在开始主页中导出项目和删除项目，以便更好地管理与分享项目。

**6.【手机自动化】**

- 企业版支持 [手机自动化](Studio/process/developProject/MobileDevicesManage/Download.md) 操作，实现在 PC 端可以操作手机上的各元素。

### 改进与增强

**1.【项目管理】**

- 优化了项目打开速度，较之前更快，提升用户体验。
- 优化了复制粘贴组件速度，较之前更快，提升用户体验。  
- 发布项目前，对项目的正确性进行校验。
- 支持新增序列或流程图作为子流程。
- 导出项目时，支持导出后选择是否打开所在文件夹。
- 导入项目时，支持导入后选择是否立即打开该项目。
- 统一了项目名称及流程包名称的命名规则，避免发布流程时名称校验不通过。
- 支持更详细的项目打开及编译错误描述，更易定位错误位置。
- 增强了 **表达式编辑器** 的 **智能感知** 功能，支持变量/参数/方法名称联想。
- 在创建变量/参数时，支持快速创建 DataTable / IUiObject 类型的变量/参数。
- 支持通过编辑区域的组件的右键菜单来访问组件的帮助文档。
- 优化 **导出项目** 功能，当导出组件项目时，导出文件的扩展名为 egs，以区别于流程项目的 dgs 文件。
- 优化导出项目和 [发布项目](Studio/process/PublishProject.md)：支持将依赖项导出到流程包中。
- 支持显示所有文件、包括在项目中/从项目中排除，方便发布项目时从项目中排除某些文件。

**2.【辅助工具】**

- 支持 Java 扩展。你可以使用 Java 扩展识别一些原本无法识别的桌面 Java 应用中的元素。
- 优化 UIA3 录制技术，提升稳定性。

**3.【可视化编辑器】**

- 在 **开始菜单页** 中优化调整了 **流程市场**、**组件市场** 等应用的入口位置。
- 将部分弹窗更改为浮窗，提升用户体验。
- 优化了日志输出界面，由左侧显示更改为编辑器底部显示，使之更全局化，提升用户体验。
- 针对社区版许可证超出配额的情况，增加了解决方法的提示。
- 更换了安装框架，优化了安装/升级体验，解决了由杀毒软件导致的安装失败问题。
- 支持非管理员权限运行编辑器时，元素识别时高亮外层窗体，并在点击时提示。
- 项目运行或调试过程中，输出面板对当前过程进行提示，使用户更加明确当前执行过程。
- 优化了搜索组件功能：在组件面板中，支持按组件名称拼音的首字母模糊搜索组件名，提升用户使用体验。
- 优化了发布窗口：在发布窗口中新增项目属性信息，如，项目名称、最新版本号等，方便用户发布流程时更清晰的查看该项目的基本信息。
- 优化了表达式编辑器输入体验：在组件属性框中写代码时，自动补全后面的括号，如，xx.ToString—> xx.ToString()。
- 优化了选择器编辑器：在选择器编辑器节点属性列表中新增了 URL 属性，实现如果页面 Title 未设定时，则使用 URL 来定位页面。
- 优化了选择器编辑器：在选择器编辑器节点属性列表中，AutomationId/ClassName/Name 这些属性的值支持输入通配符。
- 新增 **打开文件**、**打开目录**、**日期** 等参数类型，执行流程时，采用手动选择的方式代替手动输入，提升用户体验。
- 优化组件批注：支持组件批注快捷键 **Shift+F2**。
- 优化属性面板界面样式，更改背景色，提升视觉效果。
- 优化项目面板、组件面板样式，更换图标、间距，提升视觉效果。
- 优化软件许可协议界面的勾选区域，点击勾选框旁边的文字也可勾选中，提升用户体验。
- 优化版本控制中的版本比对功能的呈现样式为可折叠的树形结构，提升用户使用体验。
- 优化F4快捷键录制技术后台切换逻辑，可以更智能地自动判断并选择最合适的录制技术，提升用户使用体验。

**4.【开放市场】**

- 优化 [管理市场](Studio/market/Market.md)、[代码市场](Studio/market/NuGetMarket.md)、[组件市场](Studio/market/activityMarket.md) 界面样式：由原来的弹框形式优化为标签页形式。

### 问题修复

1. 修复了表达式编辑时，自动补入变量名不齐全的问题。
2. 修复了调试时不能查看容器类组件中最后一个组件的属性的问题。
3. 修复了搜索组件时，搜索结果展示不全的问题。
4. 修复了修改变量值后，调试项目时，修改不生效的问题。
5. 修复了编辑器界面偶尔无法点击的问题。
6. 修复了点击组件：在指定元素时，按下 F2 延迟操作时，不支持再次点击指定元素，防止出现异常。

## 组件库

![组件库功能](https://docimages.blob.core.chinacloudapi.cn/images/activities.png)

### 功能点列表

**1.【界面自动化】**

- [匹配图片](Activities/UIAutomation/MatchImage.md)：实现在指定范围内寻找指定图片，返回符合的结果集。
- [设置焦点](Activities/UIAutomation/SetFocus.md)：实现为指定元素设置焦点，支持桌面端和浏览器端。
- [选择多个项目](Activities/UIAutomation/SelectMultipleItems.md)：实现多个项目的同时选择，此组件仅当原页面支持多选时生效。
- [高亮](Activities/UIAutomation/Highlight.md)：实现指定元素高亮，可选择颜色和时间。
- [等待元素属性值](Activities/UIAutomation/WaitElementAttributeValue.md)：实现等待指定元素的属性值为指定值时，才执行下一个组件，否则会在超时时间范围内一直等待。
- [获取元素属性值](Activities/UIAutomation/GetElementAttributeValue.md)：实现获取指定元素的属性值，并将其存储在输出变量属性值中。
- OCR > [获取 OCR 文本](Activities/UIAutomation/OCR/GetOCRText.md)（企业版）：实现对指定元素或图片进行 OCR 并返回结果。
- OCR > [获取含 OCR 文本的元素](Activities/UIAutomation/OCR/GetSpecificTextOCRElement.md)（企业版）：实现对指定元素或图片进行 OCR 并查找包含指定文本的元素，结果保存在属性 OCR 元素内。
- OCR > [判断 OCR 文本是否存在](Activities/UIAutomation/OCR/IdentifyOCRTextExist.md)（企业版）：实现对指定元素或图片进行 OCR 并判断指定文本是否存在，结果保存在属性 OCR 元素内。
- 桌面控件专有：[获取焦点控件](Activities/UIAutomation/DesktopOnly/GetFocus.md)、[切换控件](Activities/UIAutomation/DesktopOnly/SwitchControl.md)，这两个控件仅在企业版中支持。
- SAP：[登录应用](Activities/UIAutomation/SAP/SAP_Login.md)、[获取状态栏信息](Activities/UIAutomation/SAP/SAP_GetStatus.md)、[选择日期](Activities/UIAutomation/SAP/SAP_SelectCalendar.md)、[选择 SAP 项](Activities/UIAutomation/SAP/SAP_Select.md)、[执行事务](Activities/UIAutomation/SAP/SAP_Transaction.md)，仅在企业版中支持这些组件。
- [截屏](Activities/UIAutomation/Screenshot.md)，实现截图，并将结果保存在指定位置或变量中。
- 支持 360 安全浏览器。新增浏览器的支持类型，使您可以操作 360 安全浏览器。
- 界面自动化架构调整，增强稳定性。
- [坐标点击](Activities/UIAutomation/Coordinate.md)：根据绝对坐标点击指定的用户界面元素。
- [移动鼠标](Activities/UIAutomation/MoveMouse.md)：移动鼠标光标位置。
- [获取鼠标位置](Activities/UIAutomation/GetMousePosition.md) 组件：获取鼠标最终光标位置。
- 屏幕文本化：[获取屏幕文本](Activities/UIAutomation/ScreenText/GetScreenText.md)、[获取屏幕含某文本的元素](Activities/UIAutomation/ScreenText/GetTextElement.md)、[判断屏幕文本是否存在](Activities/UIAutomation/ScreenText/IdentifyScreenTextExist.md)、[点击屏幕文本](Activities/UIAutomation/ScreenText/ClickScreenText.md)。
- [鼠标拖动](Activities/UIAutomation/DragDrop.md)：实现模拟鼠标按下拖动的操作，如，按下鼠标左键将文件拖动至另一文件夹内。
- 界面自动化 > [设置Web元素属性值](./Activities/UIAutomation/SetWebElementAttributeValue.md)，提升实施人员开发效率。


**2.【软件自动化】**

-  PDF：[合并文件](Activities/AppAutomation/PDF/MergePDF.md)、[提取为新文档](Activities/AppAutomation/PDF/ExtractToNewFile.md)、[获取页数](Activities/AppAutomation/PDF/GetPageNumbers.md)、[读取图片](Activities/AppAutomation/PDF/ExtractImages.md)、[读取文本](Activities/AppAutomation/PDF/ExtractText.md)
- Office Excel > [刷新透视表](Activities/AppAutomation/OfficeExcel/RefreshPivotTable.md)：实现刷新指定透视表的数据。
- Office Excel > [创建透视表](Activities/AppAutomation/OfficeExcel/CreatePivotTable.md)：实现在 Excel 中创建透视表。
-  邮件：[获取邮件(Exchange)](Activities/AppAutomation/Mail/GetExchangeMail.md) 、 [发送邮件(Exchange)](Activities/AppAutomation/Mail/SendExchangeMail.md)
-  Office Excel > [ 重置密码](Activities/AppAutomation/OfficeExcel/OfficeExcelResetPassword.md)：在 **打开/新建** 组件中使用，对 Excel 文件进行增加、更新或清除密码。
-   邮件：[获取邮件(Outlook)](Activities/AppAutomation/Mail/GetOutlookMail.md)、[发送邮件(Outlook)](Activities/AppAutomation/Mail/SendOutlookMail.md)。
-   Office Excel > [插入图片](Activities/AppAutomation/OfficeExcel/InsertPicture.md)：实现指定单元格插入图片。
- Office Excel > [设置文字颜色](Activities/AppAutomation/OfficeExcel/SetTextColor.md) ：使用拾色器提升颜色设置体验。
- 邮件 > [获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md)，使用 IMAP 服务获取邮件，同时可使用代理。
-  Office Excel > [自动填充](Activities/AppAutomation/OfficeExcel/AutoFillRange.md)，支持从源单元格区域自动填充数据到目标区域。
- Office Excel ：[分列](Activities/AppAutomation/OfficeExcel/OfficeExcelTextToColumns.md)、[复制粘贴区域](Activities/AppAutomation/OfficeExcel/OfficeExcelCopyAndPasteArea.md)。
- 浏览器 > [关闭浏览器](./Activities/AppAutomation/Browser/BrowserClose.md)：支持关闭所有类型的已打开的浏览器。
- Office Excel > [取消单元格合并](./Activities/AppAutomation/OfficeExcel/UnMergeCells.md)：实现对指定单元格区域已合并的单元格进行拆分。
- 浏览器 > [打开浏览器](./Activities/AppAutomation/Browser/OpenBrowser.md)：支持流程运行时的浏览器静默运行]，实现机器人后台工作，不干扰前端业务人员，提升用户使用体验。
- 软件自动化 > Office Excel > [替换](./Activities/AppAutomation/OfficeExcel/OfficeExcelReplace.md)，提升实施人员开发效率。
- 软件自动化 > Office Excel > [筛选](./Activities/AppAutomation/OfficeExcel/Filter.md)，允许筛选条件中的值为变量类型，扩展了筛选功能的适用范围。

**3.【代码工具】**

-  数组处理：[初始化数组](Activities/CodeExecuter/ArrayProcessing/InitializeArrayActivity.md)、[元素是否存在](Activities/CodeExecuter/ArrayProcessing/ExistsInArrayActivity.md)、[获取数组长度](Activities/CodeExecuter/ArrayProcessing/GetLengthOfArrayActivity.md)
-  HTTP > [下载文件](Activities/CodeExecuter/HTTP/HTTPDownload.md)
-  JSON > [序列化](Activities/CodeExecuter/JSON/SerializeObject.md)：可将.NET 对象序列化为 JSON 字符串。
-  JSON > [反序列化](Activities/CodeExecuter/JSON/DeserializeObject.md)：可将 JSON 字符串反序列化为.NET 对象。
-  HTTP > [HTTP 请求](Activities/CodeExecuter/HTTP/HTTPRequest.md)：实现发送 HTTP 请求并返回响应的数据，并支持测试配置的 HTTP 请求是否可用。
- 文本处理：[验证文本有效性](Activities/CodeExecuter/TextProcessing/VerifyTextActivity.md)、[提取文本](Activities/CodeExecuter/TextProcessing/ExtractTextActivity.md)、 [替换文本](Activities/CodeExecuter/TextProcessing/ReplaceTextActivity.md)、[截取文本](Activities/CodeExecuter/TextProcessing/GetSubstringActivity.md)、[获取文本长度](Activities/CodeExecuter/TextProcessing/GetLengthOfTextActivity.md)、[获取文本索引](Activities/CodeExecuter/TextProcessing/GetIndexOfTextActivity.md)
- 集合处理 ：[对象是否存在](Activities/CodeExecuter/CollectionProcessing/ExistsInCollectionActivity.md)、[添加对象](Activities/CodeExecuter/CollectionProcessing/AddToCollectionActivity.md)、[清空对象](Activities/CodeExecuter/CollectionProcessing/ClearCollectionActivity.md)、[移除对象](Activities/CodeExecuter/CollectionProcessing/RemoveFromCollectionActivity.md)、[获取集合长度](Activities/CodeExecuter/CollectionProcessing/GetLengthOfCollectionActivity.md)、[初始化集合](Activities/CodeExecuter/CollectionProcessing/InitializeCollectionActivity.md)
- 数据处理 > [数据格式化](Activities/CodeExecuter/DataProcessing/FormatData.md)：可实现对输入数据按照数值、日期和时间、货币和百分比进行格式化。
- 文本处理 > [生成 GUID ](Activities/CodeExecuter/TextProcessing/GenerateGUIDActivity.md)：实现生成一个新的 GUID。
- 类型转换：[文本转日期和时间](Activities/CodeExecuter/TypeConversion/TextToDateActivity.md)、[数组转集合](Activities/CodeExecuter/TypeConversion/ArrayToCollectionActivity.md)、[集合转数组](Activities/CodeExecuter/TypeConversion/CollectionToArrayActivity.md)。
- Python：[安装 Python](Activities/CodeExecuter/Python/PythonInstall.md)、[Python 环境](Activities/CodeExecuter/Python/PythonScope.md)、[执行 Python 代码](Activities/CodeExecuter/Python/PythonExcuteFile.md)。
- 字典：[初始化字典](./Activities/CodeExecuter/Dictionary/InitializeDictionaryActivity.md)、[添加键值对](./Activities/CodeExecuter/Dictionary/AddDictionaryActivity.md)、[获取键值对数量](./Activities/CodeExecuter/Dictionary/GetQuantityOfDictionaryActivity.md)、[是否包含键/值](./Activities/CodeExecuter/Dictionary/ContainsKeyValueActivity.md)、[移除键值对](./Activities/CodeExecuter/Dictionary/RemoveKeyValueActivity.md)、[清空字典](./Activities/CodeExecuter/Dictionary/EmptyDictionaryActivity.md)。
- 类型转换 > [文本转数值](./Activities/CodeExecuter/TypeConversion/TextToNumbericActivity.md)，实现将文本转换为数值。
- 文本 ：[分割文本](./Activities/CodeExecuter/TextProcessing/SplitTextActivity.md)、[追加文本](./Activities/CodeExecuter/TextProcessing/AppendTextActivity.md)。
- 代码工具 > PowerShell > [执行PowerShell代码](./Activities/CodeExecuter/PowerShell/PowerShell.md)，提升实施人员开发效率。
- 代码工具 > [HTTP请求](./Activities/CodeExecuter/HTTP/HTTPRequest.md)，在原有C#代码模式基础之上，新增支持纯文本输入模式。

**4.【操作系统功能调用】**

-  文件 > [重命名文件或文件夹](Activities/System/File/RenameFileOrFolder.md)：实现对指定文件或文件夹重命名。
- [输入密码](Activities/System/InputPasswordDialogActivity.md)：提供人机交互界面，弹框形式接收用户输入的密码值并可以输出输入的密码。
- [提示框](Activities/System/PromptBox.md)：用于在 Windows 桌面右下角展示在流程中必要的提示信息。
- 文件 > [遍历文件夹](Activities/System/File/ForeachFolder.md)：遍历指定的文件夹并获取文件路径，可在此组件范围内根据实际业务需要拖入其他组件。
- [下拉选择框](Activities/System/DropdownListDialog.md)：方便在流程中弹出下拉选择框形态的用户交互界面。
- [设置日期和时间](Activities/System/SetDateTime.md)：实现指定日期和时间并输出 DateTime 类型结果。
- [选择文件](Activities/System/File/SelectFile.md)：指定筛选的文件类型，在运行时弹窗选择文件后输出。
- [选择文件夹](Activities/System/File/SelectFolder.md)：选择文件夹路径，在运行时弹窗选择文件夹后输出。
- [设置剪贴板文本](Activities/System/SetContentsToClipboard.md)：实现设置文本内容到剪贴板。
- [日期和时间选择框组件](Activities/System/TimePickerDialogActivity.md)：实现流程运行时弹窗让用户选择日期和时间并输出。
- 屏幕：[锁屏](Activities/System/Screen/WindowsLockActivity.md)/[解锁](Activities/System/Screen/WindowsUnlockActivity.md)，实现电脑锁屏时，支持在 web 自动化操作及自动解锁屏幕。
- [多项选择框](./Activities/System/MultiSelectListBoxActivity.md)：实现以弹框的形式，选择一个或多个选项。
- 系统 > 文件 > [压缩文件/文件夹](./Activities/System/File/CompresseFile.md)、[解压缩文件](./Activities/System/File/DeCompresseFile.md)，提升实施人员开发效率。


**5.【数据表】**

 - [追加到 CSV 文件](Activities/DataTable/AppendToCSV.md)：实现将数据表追加到已有 CSV 文件。


**6.【流程控制】**

- [赋值（多个）](Activities/WorkflowControl/MultipleAssign.md)：支持对最多 10 个变量进行赋值。
- 判断 > [条件(Switch)](Activities/WorkflowControl/Determine/Switch.md)：实现指定 C# 表达式，并根据每个 Case 判断执行符合条件的流程。
- [状态机](Activities/WorkflowControl/StateMachine/StateMachine.md)：实现基于状态机范例的工作流程。
- [重试](Activities/WorkflowControl/Retry.md)：当执行的流程符合条件且遇到错误时尝试再次执行。
- [抛出异常](Activities/WorkflowControl/Throw.md)：在流程执行时主动抛出异常。
- [重新抛出异常](Activities/WorkflowControl/ReThrow.md)：在流程执行时重新将异常的原始信息抛出。
- [终止流程](Activities/WorkflowControl/Abort.md)：实现当执行到此组件时立即结束当前流程，不再执行后续流程。
- [调用流程（引用项目）](Activities/WorkflowControl/InvokeReferencedWorkflow.md)：实现调用已引用的项目的流程文件，供当前项目流程使用。

**7.【控制台相关】**

- [文档理解](Activities/Console/DocReader.md)：内置文档理解组件，只要控制台部署了文档理解服务，就可以使用文档理解的功能。
- [获取资产](Activities/Console/GetAssets.md)：可以直接在流程中，使用 获取资产组件，获取在控制台保存的数据资产。
- [下载文件](Activities/Console/FileDownloadActivity.md)：下载云扩 RPA 控制台“数据中心 > 文件服务”中已上传的文件。
- [上传文件](./Activities/Console/FileUploadActivity.md)、[删除文件/文件夹](./Activities/Console/FileDeleteActivity.md)。

**8.【触发器】**

- [文件触发器](Activities/Triggers/FileTrigger.md)：用于监听指定文件夹下文件变化，设置特定触发条件并自动执行流程。
- [邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md)：用于监听 Outlook 邮箱接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。
- [邮件触发器(Exchange)](Activities/Triggers/ExchangeTrigger.md)：用于监听 Exchange 服务器接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。
- [邮件触发器(IMAP)](Activities/Triggers/IMAPTrigger.md)：用于监听支持 IMAP 协议的邮箱接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。

**9.【AI Hub】**

- [证照识别](Activities/AIHub/IdentificationOfCredentials.md)：默认使用当前用户登录权限，识别证照信息。
- [票据识别](Activities/AIHub/BillIdentification.md)：默认使用当前用户登录权限，识别票据信息。
- [通用文字识别](Activities/AIHub/GeneralCharacterRecognition.md)：默认使用当前用户登录权限，识别通用文字信息。

### 改进与增强

**1.【界面自动化】**

- 界面自动化下的组件全部新增了超时属性，实现控制组件的执行时间，在超过指定时间后停止。
- **获取含 OCR 文本的元素**、**判断 OCR 文本是否存在** 组件的文本属性支持正则表达式，实现更灵活的文本查找。
- 优化了钉钉程序内元素识别，使得录制技术 UIA 可识别大部分元素。
- 增强桌面录制技术 UIA3 识别微信，实现获取文本、选择项目时可以自动滚动联系人列表操作。
- 增强 JAVA 应用在不同分辨率 DPI 下的识别回放。
- 点击组件新增了快捷辅助键属性。如，你可以在点击的同时按下 **Ctrl** 键。
- 浏览器端支持 **图像识别** 功能，使复杂场景下元素可以识别到。
- 对于桌面应用，**输入文本** 组件支持 **清空文本** 操作，使用户可以在输入文本之前清除输入框的原有文本。
- **获取区域文本** 组件更名为 **获取区域结构**（企业版）。
- **悬停** 组件支持图像识别。扩大识别场景，当原生识别不稳定时，提供图像识别定位元素方法。
- 支持在金蝶 EAS 系列软件中，对报表类型界面通过 **获取结构化数据** 获取报表数据。
- 在图像识别模式下，**等待元素出现** 组件返回的控件元素为图象，而非锚点，使用户可以取图像输出执行后续操作。
- 加强对用友 NC, U8 系列软件的支持。比如自定义按钮，报表可以识别和抓取。
- 浏览器支持增强：支持内嵌 IE 浏览器中元素的识别，例如部分界面使用 IE 内核渲染的网页（chm 文件）；支持 360 安全浏览器兼容模式下元素的识别。
- 选择器编辑器中 Java 应用的 Name 属性全部层级支持通配符。
- 优化了选择器编辑器界面，使得用户操作体验更友好。
- 界面自动化组件支持即刻优雅终止流程。
- 优化了界面自动化 > [选择项目](Activities/UIAutomation/SelectItem.md) 组件：项目文本输入框优化为下拉框，与其它同系列组件保持一致。
- 优化了获取元素属性值、等待元素属性值、属性校验组件，使其识别能力增强。
- 针对 [获取元素属性值](Activities/UIAutomation/GetElementAttributeValue.md)、[等待元素属性值](Activities/UIAutomation/WaitElementAttributeValue.md)、[属性校验](Activities/Check/AttributeCheck.md) 这些组件，支持获取自定义属性。
- [选择器编辑器](Activities/Appendix/Selector.md) 支持验证属性值为变量（变量需有默认值）的情况、支持验证多个相同元素，提升用户体验。
- [选择器编辑器](Activities/Appendix/Selector.md)/[元素探测器](Activities/Appendix/UiDetector.md) 的属性值支持常量变量混合输入、支持识别用户界面元素所需的所有元素并按已应用和未应用状态进行分类展示，提升用户体验。
- [发送快捷键](./Activities/UIAutomation/SendHotkey.md)：新增发送前行为属性，支持点击和设置焦点两种行为。


**2.【软件自动化】**

- Office Excel > [获取末列号](Activities/AppAutomation/OfficeExcel/GetLastColumn.md)：增加了输出字母和数字列号。
- [发送邮件(SMTP)](Activities/AppAutomation/Mail/SendMailSMTP.md)、[获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md)、[获取邮件(POP3)](Activities/AppAutomation/Mail/GetMailPOP3.md) 组件支持手动选择安全方式。
- [获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md) 组件支持仅获取未读邮件。
- 优化了 Office Excel > [排序](Activities/AppAutomation/OfficeExcel/Sort.md) 组件，支持指定开始行号。
- 优化了 Office Excel > [设置单元格背景色](Activities/AppAutomation/OfficeExcel/SetCellBackcolor.md) 组件，使用拾色器提升颜色设置体验。
- 提升 Office Excel 系列组件执行性能。
- 化化了浏览器系列组件：在 [打开浏览器](Activities/AppAutomation/Browser/OpenBrowser.md)、[当前页跳转](Activities/AppAutomation/Browser/NavigateTo.md)、[刷新浏览器](Activities/AppAutomation/Browser/RefreshBrowser.md) 中增加了“等待加载完成”这个可选项属性，实现当页面全部加载完成后组件才算执行成功。
- Office Excel > [查找](Activities/appautomation/officeexcel/Search.md)：支持模糊查找和精确查找，给用户带来更灵活、更方便的操作体验。
- Office Excel > [排序](./Activities/AppAutomation/OfficeExcel/Sort.md)，支持选择排序方式。
  
**3.【流程控制】**

- 提升 [调用流程](Activities/WorkflowControl/InvokeWorkflow.md) 组件体验，点击 **导入参数** 可直接将子流程参数导入。
- 优化重试组件：支持该组件 **重试间隔** 属性的默认值为时间格式（00: 00: 00），避免用户输入错误，提升用户输入体验。
- [重试](./Activities/WorkflowControl/Retry.md)，将条件属性归类至可选项类别中。

**4.【触发器】**

- [文件触发器](Activities/Triggers/FileTrigger.md)： 增加了输出监听的文件路径。
- 邮件触发器：[邮件触发器(IMAP)](Activities/Triggers/IMAPTrigger.md)、[邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md) 和 [邮件触发器(Exchange)](Activities/Triggers/ExchangeTrigger.md) 增加了输出监听到的新邮件。

**5.【操作系统功能调用】**

- 优化了系统 > 文件 > [新建文件/文件夹](Activities/System/File/NewFileOrFolder.md) 组件，增加“同名替换”可选项属性，实现新建文件/文件夹时，如果存在同名情况，则覆盖替换。
- 优化了校验 > [属性校验](Activities/Check/AttributeCheck.md) 组件：在属性校验组件的属性名下拉框中仅显示当前元素支持的属性。
- 优化了校验 > [值校验](Activities/Check/ValueCheck.md) 组件：增加“开始于/结束于”校验条件，实现某字符串是否以指定字符串的字符开头和结束校验功能。
- 优化[确认框](./Activities/System/ConfirmDialog.md)、[输入框](./Activities/System/InputDialog.md)，支持可以手动复制“描述”信息。

**6.【代码工具】**

- C# > [执行 C#代码](Activities/codeexcuter/../CodeExecuter/CSharp/ExecuteCSharp.md)：支持类、函数的编写，增强组件功能。
- C# > 执行C#代码，支持输出出错的具体代码位置（行号）及错误信息。

**7.【数据库】**

- 数据库系列组件（[执行语句](Activities/Database/ExecuteNonQuery.md)、[查询](Activities/Database/Select.md)）：支持根据实际情况设置超时，以适用不同的应用场景。
- [连接数据库](./Activities/Database/ConnectDatabase.md)：优化连接 DB2 数据库界面提示信息。

**8.【控制台相关】**

- [文档理解](./Activities/Console/DocReader.md)：支持识别图片类型文件。

## 机器人

![机器人功能](https://docimages.blob.core.chinacloudapi.cn/images/robot.png)

### 功能点列表

**1.【流程管理】**

- 新增 [定时任务](Robot/CronJob.md) 功能，使得原本需要采购控制台完成的功能，在机器人中便可完成。
- 支持获取并运行 [云扩流程市场](Robot/ProcessMarket.md) 中的流程。
- 在执行流程时，支持权限配置。具体功能请参见 [流程库](Robot/localworkflow.md)。
- 执行本地流程时支持填写流程参数，详见 [执行本地流程](Robot/localworkflow.md)。
- 在新建定时任务时支持 [按 Cron 表达式](Robot/CronJob.md) 配置定时任务，以满足用户自定义定时任务场景。
- 支持流程 [执行过程截图](Robot/localworkflow.md)，方便运维人员排查及追踪异常。
- 支持防止流程执行 [超时](Robot/localworkflow.md)：若运行时间超过设定的时间时则终止流程。如，勾选“超时时间 1 小时”，表示超过 1 小时未执行完流程，则终止流程。
- 优化执行流程时 [参数的设置方式](Robot/localworkflow.md)：新增 **打开文件**、**打开目录**、**日期** 等参数类型，执行流程时，采用手动选择的方式代替手动输入，提升用户体验。
- 优化 [流程市场界面](Robot/ProcessMarket.md)，鼠标悬浮于任意流程时，即可显示“运行”按钮，提升用户使用体验。
- 优化定时任务，在定时任务开始前30秒弹窗提示，避免影响用户手头工作。
- 优化执行流程时桌面右下角机器人图标，使得机器人图标闪动效果更明显。
- 支持在[流程执行页面](./Robot/RunningProcess.md)打开日志文件，提升用户使用体验。

**2.【基础配置】**

- 在 **设置** 页面中，新增 [关于页](Robot/Settings/About.md)，可查看软件版本、许可证有效期及更改激活方式。
- 在基础配置中，新增 **设置 > 基本** 页面，可 [配置日志与视频文件保留时间](Robot/Settings/Basic.md)。
- 新增 [IBM DB2 扩展](./Robot/Settings/extensions/DB2Extension.md)来进行IBM DB2 数据库的自动化。
- 企业版支持配置[是否接收控制台调度](./Robot/Settings/Basic.md)，使得机器人未执行控制台调度命令时，仍然可以继续使用该机器人。

**3.【信息管理】**

- 新增 [正在执行](Robot/RunningProcess.md) 页面，可以查看正在执行的流程相关信息。
- 新增机器人 [概览页](Robot/Overview.md)，可展示当前机器人全局数据。
- 新增 [流程执行历史页](Robot/ProcessHistory.md)，可展示流程执行的历史记录。
- 优化 [概览界面](Robot/Overview.md)：对于无定时任务和无最近执行流程时，支持关联对应的页面，引导用户使用，提升操作体验。
- 优化[正在执行](./Robot/RunningProcess.md)界面，将标题改为“执行日志”并增加“再次执行”按钮。

### 改进与增强

**1.【流程管理】**

- 优化了停止正在运行流程的操作：支持按热键 Shift+F5 终止当前正在运行的流程，方便快捷。

**2.【信息管理】**

- 优化了安装后体验：不用激活就可使用流程市场等功能。

**3.【基础配置】**

- 优化了机器人的关于页面，当企业版用户使用本地激活方式激活后，在该页可查看许可证有效期。

## 控制台

![控制台](https://docimages.blob.core.chinacloudapi.cn/images/console.png)

### 功能点列表 

**1.【RPA 管理】**  

- [调度队列](Console/queue/aboutqueue.md)：主要用于对机器人集群进行管理调度，实现队列中 RPA 流程任务动态分配，提升机器人及任务运行效率。
- [任务记录](Console/job/aboutJob.md)：主要用于记录并展示所有流程任务的执行状况，对任务执行日志进行综合管理。你可以通过这个页面查看任务的执行情况和结果，也可以通过这个页面查看任务日志。
- 流程部署时支持使用资产管理定义的账户密码凭证及参数进行赋值以执行流程。
- 流程部署、调度队列及任务记录中支持对任务优先级进行调整，便于调整任务执行顺序。
- 机器人管理页面中新增托管状态，未托管的机器人将不受控制台任务调度。
- 在调度队列详情中增加任务列表，便于快速管理队列任务。
- 支持用户删除调度队列。


**2.【文档理解】** 

- [文档理解](Console/docreader/aboutDocreader.md)：云扩智能文档理解服务利用 OCR、NLP 等技术辅助您快速对各类文档、表格、文 本、证照等进行信息抽取、审阅、登记、流程判断。您可以自定义上传图片、PDF 等格式模板文件，通过框选方式确定需要拖动的文本区域来快速配置模板。
- [文档理解](Console/docreader/aboutDocreader.md)，通过组件调用当前模板服务，从而实现 RPA 流程大量抽取非结构化文本信息。

**3.【数据中心】**  

- [资产管理](Console/datacentor/asset/AboutAsset.md)：主要用于定义各类账户密码凭证、参数等, 可供各类 RPA 流程进行调用。
- [文件服务](Console/datacentor/fileservice/Aboutfileservice.md)：支持文件夹的增删改以及文件上传、下载等操作，同时向 RPA 流程提供各类文件服务。
  
**4.【全局管理】**

- [许可证](Console/management/license/aboutLicense.md) 页面增加文档理解次数控制，用于对文档理解的模板调用次数进行控制。 

**5.【仪表盘】**

- 新增 [机器人监控仪表盘](robot/../Console/dashboard/RobotDashboard.md)：支持自定义时间段查询机器人运行状况，如，可用机器人执行任务总数/忙碌总时长/平均忙碌比/故障占比 TOP/状态分布/忙碌 TOP 等等。
- 新增 [队列监控](Console/dashboard/QueueDashboard.md) 功能，多维度对队列中机器人、流程任务运行调度情况进行统计监测：

  * 统计队列数量、队列任务时长、流程部署数量、机器人数量、机器人忙碌比；
  * 统计分析队列成功占比 TOP 10、队列故障占比 TOP 10；
  * 统计调度队列任务状态分布情况；
  * 展示调度队列忙碌情况及执行流程情况；
  * 统计调度队列任务平均等待时长 TOP 10。
  
**6.【首页】**

- 控制台首页中新增手机自动化（IOS 和 Android）安装包。 

**7.【登录及注册】**

- 控制台前端新增超时自动退出系统机制，提升系统安全性。
- 用户注销后，token 自动过期且不支持访问 API，提升系统安全性。

**8.【Console 管理后台】**

新上线 Console 管理后台，用于对控制台租户、账户等进行管理，主要包括：
- 新增通过后台查看并管理租户信息。
- 新增通过后台删除租户。
- 新增通过后台创建企业版租户及管理员账号。
- 新增通过后台对控制台用户邮箱后缀进行管理。

### 改进与增强

**1.【登录及注册】**

- 升级登录注册页面样式及交互，提升登录注册用户体验。

**2.【仪表盘】**

- 优化仪表盘数据统计方式，提升系统性能。
- 优化仪表盘数据保留方式。
- 优化仪表盘时间筛选问及保留精确位数问题。

**3.【全局管理】**

- 优化审计日志、仪表盘中时间查询问题。
- 统一系统内用户姓名、个人姓名，优化部分姓名数据同步机制。
- 优化系统告警提示语。
- 优化系统邮件发送模板。

## 云扩小程序

![小程序](https://docimages.blob.core.chinacloudapi.cn/images/panel.png)

### 功能点列表

**1.【可视化编辑器】**

- 全局组件：新增顶部导航、左侧导航组件，支持应用内多页面跳转。
- 模板组件：新增流程组件，支持一键启动控制台流程。
- 新增全新的 [数据表管理](Apps/devApps/appsedit/TableManagement/TableManage.md) 功能：
    - 支持用户通过导入或新建的方式在小程序里创建数据表。
    - 丝滑易用的数据处理：支持即时修改响应，区域复制粘贴，拖拽覆盖等方法帮助用户快速修改数据。
    - 强大的公式系统：支持单元格公式计算及数据引用，构造表数据的多样性。
    - 构建数据可视化操作：支持多种列格式，定义适合用户的编辑形式。
    - 快捷查找：提供多样筛选排序功能，快速分析整理数据。
    - 强大的协作功能：支持多用户共同对表的修改，保证数据正确响应
-  构建更强大的交互页面
    - 新增模块组件：[表格](Apps/devApps/appsedit/component/ModuleComponents/Table.md)、[表单](Apps/devApps/appsedit/component/ModuleComponents/Form.md)、[描述列表](Apps/devApps/appsedit/component/ModuleComponents/DescriptionList.md)、[OCR 结果对比](Apps/devApps/appsedit/component/ModuleComponents/CompareOCRResult.md)。
    - 通过组件自定义页面与数据表交互，让终端用户可以轻松地通过界面操作数据表。
- [任务记录](Apps/devApps/appsedit/component/ModuleComponents/TaskLog.md) 模块组件，可以通过任务记录列表查看任务信息、当前状态及日志等信息。
- 新增输入、展示、布局系列组件。
- 新增组件的通用配置、通用样式、事件与行为。
- 新增[变量管理](./Apps/devApps/appsedit/BasicOperation.md)功能，使得每个小程序独享一套全局变量。
- 在小程序编辑页面中，支持复制已创建的页面、组件。
- 在小程序模拟界面中，支持拖拽改变组件的层级，使组件置于不同的视图下。

**2.【小程序开发库】**

- 支持应用版本管理，控制台统一对应用进行上下架及版本管理。
- 支持在 **关于我们** 页面查看小程序系统的版本号，便于系统版本管理。
- 新增进入云扩论坛、云扩学院的快捷入口。
- 支持在小程序开发页面，复制小程序功能。

**3.【小程序工作站】**

- 支持 **我的应用** 查找并运行。
- 支持在我的小程序页面，复制小程序URL功能，方便用户分享我的小程序。

### 改进与增强

**1.【可视化编辑器】**

- 优化了 logo 及产品更名：原工作台/应用，更名为小程序 。
- 全面优化小程序编辑器交互样式，使界面更清爽、交互更简洁。
- 优化小程序界面的错误提示内容，使用户更明确。
- 优化小程序编辑界面、错误页面样式，提升用户体验。