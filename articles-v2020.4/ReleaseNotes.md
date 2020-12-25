# 云扩 RPA 产品发版说明
## 2020.12.24 发版说明
2020.12.24 发布了云扩 RPA ,本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 控制台   | 3.0.33343 |

你可以通过[云扩控制台](https://console.encoo.com/)下载并体验相关产品。

### 新增功能

#### 【控制台】

1. 新增[队列监控](Console/dashboard/QueueDashboard.md)功能，多维度对队列中机器人、流程任务运行调度情况进行统计监测：
    * 统计队列数量、队列任务时长、流程部署数量、机器人数量、机器人忙碌比；
    * 统计分析队列成功占比 TOP 10、队列故障占比 TOP 10；
    * 统计调度队列任务状态分布情况；
    * 展示调度队列忙碌情况及执行流程情况；
    * 统计调度队列任务平均等待时长 TOP 10。  
2. 支持用户在触发流程任务时对指定机器人进行修改，便于用户实时修改执行目标。
3. 控制台所有模块中新增顶部区域及功能提示，辅助用户了解功能，同时美化系统样式。
4. 流程部署、调度队列及任务记录中支持对任务优先级进行调整，便于调整任务执行顺序。
5. 流程部署时支持使用资产管理定义的账户密码凭证及参数进行赋值以执行流程。
6. 新增获取加密资产 API 开放给组件端进行调用。

### 改进与增强

#### 【控制台】

1. 统一系统内用户姓名、个人姓名，优化部分姓名数据同步机制。
2. 优化控制台菜单栏整体交互、样式、图标，提升视觉效果。
3. 优化控制台全局列表样式、抽屉浮窗样式，提升用户体验。
4. 优化仪表盘数据统计方式，提升系统性能。
5. 统一英文环境下界面的样式。
6. 改进前端界面对 IE 11的支持及适配效果，提升用户体验。
7. 优化审计日志、仪表盘中时间查询问题。

## 2020.12.21 发版说明
2020.12.21 发布了云扩 RPA ,本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2012.10 |
|机器人 |1.1.2012.10|

你可以通过[云扩控制台](https://console.encoo.com/)下载并体验相关产品。

### 新增功能

#### 【编辑器】
1. 企业版支持[手机自动化](Studio/process/developProject/MobileDevicesManage/Download.md)操作，实现在 PC 端可以操作手机上的各元素。
2. 支持[引用外部项目](Studio/process/ReferenceProject.md)作为依赖项，供当前流程使用。
3. 支持启用[版本控制（预览）](Studio/VersionControl.md)功能：用于记录本地项目中文件内容的变化，以便将来查看指定版本的修订情况。
4. 支持导入文件：将其他文件导入到当前所选文件夹下。
5. 支持单个组件包括在错误捕获中：将选择的单个组件用错误捕获组件包括在Try模块中，方便调试。
6. 支持切换[激活](Studio/quickStart/Activation.md)方式：在关于页面实现社区版/企业版编辑器激活方式的切换以便重新激活。

#### 【组件库】
1. 代码工具 > 类型转换：[文本转日期和时间](Activities/CodeExecuter/TypeConversion/TextToDateActivity.md)、[数组转集合](Activities/CodeExecuter/TypeConversion/ArrayToCollectionActivity.md)、[集合转数组](Activities/CodeExecuter/TypeConversion/CollectionToArrayActivity.md)。
2. 系统 > 屏幕：[锁屏](Activities/System/Screen/WindowsLockActivity.md)/[解锁](Activities/System/Screen/WindowsUnlockActivity.md)，实现电脑锁屏时，支持在web自动化操作及自动解锁屏幕。
3. 控制台 > [下载文件](Activities/Console/FileDownloadActivity.md)：下载云扩 RPA 控制台“数据中心 > 文件服务”中已上传的文件。
4. 界面自动化 > [鼠标拖动](Activities/UIAutomation/DragDrop.md)：实现模拟鼠标按下拖动的操作，如，按下鼠标左键将文件拖动至另一文件夹内。
5. 软件自动化 > Office Excel ：[分列](Activities/AppAutomation/OfficeExcel/OfficeExcelTextToColumns.md)、[复制粘贴区域](Activities/AppAutomation/OfficeExcel/OfficeExcelCopyAndPasteArea.md)。
6. 流程控制 > [调用流程（引用项目）](Activities/WorkflowControl/InvokeReferencedWorkflow.md)：实现调用已引用的项目的流程文件，供当前项目流程使用。
7. 代码工具 > Python：[安装Python](Activities/CodeExecuter/Python/PythonInstall.md)、[Python环境](Activities/CodeExecuter/Python/PythonScope.md)、[执行Python代码](Activities/CodeExecuter/Python/PythonExcuteFile.md)。

#### 【机器人】

1. 支持流程[执行过程截图](Robot/localworkflow.md)，方便运维人员排查及追踪异常。
2. 支持防止流程执行[超时](Robot/localworkflow.md)：若运行时间超过设定的时间时则终止流程。如，勾选“超时时间1小时”，表示超过1小时未执行完流程，则终止流程。

### 改进与增强

#### 【编辑器】

1. 新增**打开文件**、**打开目录**、**日期**等参数类型，执行流程时，采用手动选择的方式代替手动输入，提升用户体验。
2. 优化**导出项目**功能，当导出组件项目时，导出文件的扩展名为 egs，以区别于流程项目的 dgs 文件。
3. 优化[管理市场](Studio/market/Market.md)、[代码市场](Studio/market/NuGetMarket.md)、[组件市场](Studio/market/activityMarket.md)界面样式：由原来的弹框形式优化为标签页形式。
4. 优化导出项目和[发布项目](Studio/process/PublishProject.md)：支持将依赖项导出到流程包中。
5. 优化组件批注：支持组件批注快捷键**Shift+F2**。
6. 支持显示所有文件、包括在项目中/从项目中排除，方便发布项目时从项目中排除某些文件。

#### 【组件库】

1. 优化重试组件：支持该组件**重试间隔**属性的默认值为时间格式（00:00:00），避免用户输入错误，提升用户输入体验。
2. 针对[获取元素属性值](Activities/UIAutomation/GetElementAttributeValue.md)、[等待元素属性值](Activities/UIAutomation/WaitElementAttributeValue.md)、[属性校验](Activities/Check/AttributeCheck.md)这些组件，支持获取自定义属性。
3. [选择器编辑器](Activities/Appendix/Selector.md)支持验证属性值为变量（变量需有默认值）的情况、支持验证多个相同元素，提升用户体验。
4. [选择器编辑器](Activities/Appendix/Selector.md)/[元素探测器](Activities/Appendix/UiDetector.md)的属性值支持常量变量混合输入、支持识别用户界面元素所需的所有元素并按已应用和未应用状态进行分类展示，提升用户体验。
5. 代码工具 > C# > [执行C#代码](Activities/codeexcuter/../CodeExecuter/CSharp/ExecuteCSharp.md)：支持类、函数的编写，增强组件功能。
6. 数据库系列组件（[执行语句](Activities/Database/ExecuteNonQuery.md)、[查询](Activities/Database/Select.md)）：支持根据实际情况设置超时，以适用不同的应用场景。
7. 软件自动化 > Office Excel > [查找](Activities/appautomation/officeexcel/Search.md)：支持模糊查找和精确查找，给用户带来更灵活、更方便的操作体验。

#### 【机器人】

1. 优化执行流程时[参数的设置方式](Robot/localworkflow.md)：新增**打开文件**、**打开目录**、**日期**等参数类型，执行流程时，采用手动选择的方式代替手动输入，提升用户体验。
2. 优化[流程市场界面](Robot/ProcessMarket.md)，鼠标悬浮于任意流程时，即可显示“运行”按钮，提升用户使用体验。
3. 优化[概览界面](Robot/Overview.md)：对于无定时任务和无最近执行流程时，支持关联对应的页面，引导用户使用，提升操作体验。

## 2020.12.10 发版说明
2020.12.10 发布了云扩 RPA ,本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 控制台（企业版）   | 3.0.31848 |

你可以通过[云扩控制台](https://console.encoo.com/)下载并体验相关产品。

### 新增功能

#### 【控制台】
1. 新增[机器人监控仪表盘](Console/dashboard/RobotDashboard.md)：支持自定义时间段查询机器人运行状况，如，可用机器人执行任务总数/忙碌总时长/平均忙碌比/故障占比TOP/状态分布/忙碌TOP等等。
2. 新增[机器人运行统计表](Console/dashboard/dashboard2.md)，支持自定义时间段查询机器人执行任务数、执行成功数、存在总时长、忙碌总时长、平均忙碌比、平均成功率等明细情况及变化走势。
3. 新增[用户流程统计表](Console/dashboard/dashboard3.md)，支持自定义时间段查询用户创建流程部署数、创建任务计划数、相应任务运行状态等明细情况及走势。
4. 新增共享机器人，支持各资源组调度队列及流程部署使用共享机器人执行任务，增加机器人利用率。
5. 流程部署支持下发命令控制机器人录制视频，日志详情页面支持查看视频录制及回放。
6. 新增控制台埋点开关，便于用户自由选择是否监测系统行为。
7. 上线新的手机验证 API 、用户列表 API ，便于打通云扩系统间数据。

### 改进与增强

#### 【控制台】
1. 升级登录注册页面样式及交互，提升登录注册用户体验。
2. 对系统服务端错误处理及前端用户提示进行优化。
3. 对系统部分页面空数据或无访问权限显示方式进行优化。
4. 修复安全问题，提升系统安全性，例如，账户密码校验规则限制、失败锁定等。
5. 优化英文版下的系统部分样式及文言。

## 2020.11.26 发版说明
2020.11.26 发布了云扩 RPA ，本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2011.12 |
| 机器人   | 1.1.2011.12 |
| 控制台   | 3.0.30440 |
| 小程序   | V1.0.1|

你可以通过[云扩控制台](https://console.encoo.com/)下载并体验相关产品。

### 新增功能

#### 【编辑器】
1. 支持流程[导出到 EXCEL](Studio/Introduction/TheUserInterface.md) 功能：鼠标右击在流程编辑区域中容器内组件（流程图/序列/状态机）的空白处，在弹出的上下文菜单中，选择“导出到 EXCEL”，实现将 XAML文件内容导出到 Excel 中，方便业务人员查看流程结构。
2. 在“开始 > 打开 > 本地项目”列表上方，新增“刷新”按钮，可手动刷新本地项目列表，实现重新加载当前路径下的项目文件夹。
3. 在“开始 > 帮助”页面，新增AI HUB 实用链接，方便用户更好地了解AI HUB 产品。
4. 在“新建 > 从模板新建”列表中，新增模块化的“[企业流程模板](Studio/process/ProjectTemplates.md)”，同时支持查看更多模板。
5. 界面自动化架构调整，增强稳定性。


#### 【组件库】
1. 系统 > [日期和时间选择框](Activities/System/TimePickerDialogActivity.md)组件：实现流程运行时弹窗让用户选择日期和时间并输出。
2. AI Hub系列组件：[证照识别](Activities/AIHub/IdentificationOfCredentials.md)、[票据识别](Activities/AIHub/BillIdentification.md)、[通用文字识别](Activities/AIHub/GeneralCharacterRecognition.md)。
3. 代码工具 > 文本处理 > [生成 GUID ](Activities/CodeExecuter/TextProcessing/GenerateGUIDActivity.md)组件，实现生成一个新的GUID。
4. 流程控制 > [终止流程](Activities/WorkflowControl/Abort.md)组件，实现当执行到此组件时立即结束当前流程，不再执行后续流程。
5. 界面自动化 > [坐标点击](Activities/UIAutomation/Coordinate.md)组件：根据绝对坐标点击指定的用户界面元素。
6. 界面自动化 > [移动鼠标](Activities/UIAutomation/MoveMouse.md)组件：移动鼠标光标位置。
7. 界面自动化 > [获取鼠标位置](Activities/UIAutomation/GetMousePosition.md)组件：获取鼠标最终光标位置。
8. 界面自动化 > 屏幕文本化系列组件（企业版）：[获取屏幕文本](Activities/UIAutomation/ScreenText/GetScreenText.md)、[获取屏幕含某文本的元素](Activities/UIAutomation/ScreenText/GetTextElement.md)、[判断屏幕文本是否存在](Activities/UIAutomation/ScreenText/IdentifyScreenTextExist.md)、[点击屏幕文本](Activities/UIAutomation/ScreenText/ClickScreenText.md)。

#### 【机器人】
1. 在新建定时任务时支持[按 Cron 表达式](Robot/CronJob.md)配置定时任务，以满足用户自定义定时任务场景。  


#### 【控制台】
1. 在数据中心新增[文件服务](Console/datacentor/fileservice/Aboutfileservice.md)功能，支持文件夹的增删改以及文件上传、下载等操作，同时向 RPA 流程提供各类文件服务。
2. 在[文档理解](Console/docreader/aboutDocreader.md)服务中，新增 OCR 抽取模型，通过组件调用当前模板服务，从而实现 RPA 流程大量抽取非结构化文本信息。
3. [许可证](Console/management/license/aboutLicense.md)页面增加文档理解次数控制，用于对文档理解的模板调用次数进行控制。  
   
#### 【小程序】
1. [任务记录](Apps/devApps/appsedit/component/workflowlog.md)模块组件，可以通过任务记录列表查看任务信息、当前状态及日志等信息。

### 改进与增强

#### 【编辑器】

1. 优化了搜索组件功能：在组件面板中，支持按组件名称拼音的首字母模糊搜索组件名，提升用户使用体验。
2. 优化了发布窗口：在发布窗口中新增项目属性信息，如，项目名称、最新版本号等，方便用户发布流程时更清晰的查看该项目的基本信息。
3. 优化了表达式编辑器输入体验：在组件属性框中写代码时，自动补全后面的括号，如，xx.ToString—>xx.ToString()。
4. 优化了选择器编辑器：在选择器编辑器节点属性列表中新增了URL 属性，实现如果页面Title未设定时，则使用URL来定位页面。
5. 优化了选择器编辑器：在选择器编辑器节点属性列表中，AutomationId/ClassName/Name这些属性的值支持输入通配符。

#### 【组件库】

1. 优化了校验 > [值校验](Activities/Check/ValueCheck.md)组件：增加“开始于/结束于”校验条件，实现某字符串是否以指定字符串的字符开头和结束校验功能。
2. 优化了系统 > 文件 >[新建文件/文件夹](Activities/System/File/NewFileOrFolder.md)组件，增加“同名替换”可选项属性，实现新建文件/文件夹时，如果存在同名情况，则覆盖替换。
3. 优化了校验 > [属性校验](Activities/Check/AttributeCheck.md)组件：在属性校验组件的属性名下拉框中仅显示当前元素支持的属性。
4. 化化了软件自动化 > 浏览器系列组件：在[打开浏览器](Activities/AppAutomation/Browser/OpenBrowser.md)、[当前页跳转](Activities/AppAutomation/Browser/NavigateTo.md)、[刷新浏览器](Activities/AppAutomation/Browser/RefreshBrowser.md)中增加了“等待加载完成”这个可选项属性，实现当页面全部加载完成后组件才算执行成功。
5. 优化了界面自动化 > [选择项目](Activities/UIAutomation/SelectItem.md)组件：项目文本输入框优化为下拉框，与其它同系列组件保持一致。
6. 优化了获取元素属性值、等待元素属性值、属性校验组件，使其识别能力增强。


#### 【机器人】

1. 优化了停止正在运行流程的操作：支持按热键 Shift+F5 终止当前正在运行的流程，方便快捷。
2. 优化了安装后体验：不用激活就可使用流程市场等功能。
3. 优化了机器人的关于页面，当企业版用户使用本地激活方式激活后，在该页可查看许可证有效期。
   
#### 【小程序】
1. 优化了logo及产品更名：原工作台/应用，更名为小程序 。

### 问题修复

#### 【组件库】
1. 修复了点击组件：在指定元素时，按下F2延迟操作时，不支持再次点击指定元素，防止出现异常。



## 2020.10.19 发版说明
2020.10.19 发布了云扩 RPA 编辑器，本次发布的产品版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2010.17 |
| 机器人   | 1.1.2010.17 |


你可以通过[云扩控制台](https://console.encoo.com/)下载并体验相关产品。

### 新增功能

#### 【编辑器】



1. 新增[新建组件项目](./Studio/process/CreateLibrary.md)，将多个可重复使用的流程封装为组件包，可发布到组件市场供其它项目使用。
2. 新增[从模板新建自动化项目](./Studio/process/ProjectTemplates.md)，支持 RPA 实施人员规范 RPA 流程开发方式，提升企业级的 RPA 流程实施质量。
3. 支持查看和编辑当前登录用户在控制台所属资源组下的流程。
4. 新增项目右击操作（打开文件夹/项目设置/添加状态机文件）。
5. 调试状态下，当发生错误时，支持忽略、重试、重启操作。
6. 当光标置于任意输入框时，支持快捷键 **Ctrl+E** 快速打开表达式编辑器。
7. 新增**开始菜单页** Homepage 视图，拆分项目编辑和非编辑操作页面，降低项目编辑过程中的干扰率，提升流程编辑效率。




#### 【组件】

1.  **软件自动化 > PDF**：[合并文件](Activities/AppAutomation/PDF/MergePDF.md)、[提取为新文档](Activities/AppAutomation/PDF/ExtractToNewFile.md)、[获取页数](Activities/AppAutomation/PDF/GetPageNumbers.md)、[读取图片](Activities/AppAutomation/PDF/ExtractImages.md)、[读取文本](Activities/AppAutomation/PDF/ExtractText.md)
2.  **系统 > 文件 > [重命名文件或文件夹](Activities/System/File/RenameFileOrFolder.md)**
3. **系统 > [输入密码](Activities/System/InputPasswordDialogActivity.md)**
4. **控制台 > [文档理解](Activities/Console/DocReader.md)**：内置文档理解组件，只要控制台部署了文档理解服务，就可以使用文档理解的功能。
5. **控制台 > [获取资产](Activities/Console/GetAssets.md)**：可以直接在流程中，使用 获取资产组件，获取在控制台保存的数据资产。
5.  **代码工具 > 数组处理**：[初始化数组](Activities/CodeExecuter/数组处理/InitializeArrayActivity.md)、[元素是否存在](Activities/CodeExecuter/数组处理/ExistsInArrayActivity.md)、[获取数组长度](Activities/CodeExecuter/数组处理/GetLengthOfArrayActivity.md)
6.  **代码工具 > HTTP > [下载文件](Activities/CodeExecuter/HTTP/HTTPDownload.md)**

#### 【机器人】

1. 新增[定时任务](Robot/CronJob.md)功能，使得原本需要采购控制台完成的功能，在机器人中便可完成。
1. 支持获取并运行[云扩流程市场](Robot/ProcessMarket.md)中的流程。


### 改进与增强

#### 【编辑器】
在**开始菜单页**中优化调整**流程市场**、**组件市场**等应用的入口位置。
#### 【组件】
1. **触发器 > [文件触发器](Activities/Triggers/FileTrigger.md)**： 增加输出监听的文件路径。
2. **触发器 > 邮件触发器**：[邮件触发器(IMAP)](Activities/Triggers/IMAPTrigger.md)、[邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md)和[邮件触发器(Exchange)](Activities/Triggers/ExchangeTrigger.md) 增加输出监听到的新邮件。
3. **软件自动化 > Office Excel > [获取末列号](Activities/AppAutomation/OfficeExcel/GetLastColumn.md)**：增加输出字母和数字列号。


## 2020.09.27 发版说明

2020.09.27 发布了云扩 RPA 编辑器、机器人和工作台，本次发布的产品版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2009.11 |
| 机器人   | 1.1.2009.11 |
| 小程序   | V1.0.0 |

你可以通过[云扩控制台](https://console.encoo.com/)下载并体验编辑器和机器人，或者申请体验工作台产品。

### 新增功能

#### 【编辑器】

1. 新增 Microsoft Edge 浏览器扩展插件，在进行自动化 Edge 操作之前，请先安装 [Microsoft Edge 扩展](Studio\Extensions\EdgeExtension.md)。
2. **选择器编辑器**新增获取 XPath 功能，可以使用 XPath 的形式对元素进行展现，参见[选择器](Activities\Appendix\Selector.md)。
3. 新增 **IE 前端日志收集器**应用程序，使用该应用程序调试用 IE 完成的 RPA 流程并获取调试日志，参见[收集 IE 前端日志工具](Activities\Appendix\IELog.md)。

#### 【组件】

1. **触发器 > [文件触发器](Activities/Triggers/FileTrigger.md)**：用于监听指定文件夹下文件变化，设置特定触发条件并自动执行流程。
1. **触发器 > [邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md)**：用于监听 Outlook 邮箱接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。
1. **触发器 > [邮件触发器(Exchange)](Activities/Triggers/ExchangeTrigger.md)**：用于监听 Exchange 服务器接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。
1. **触发器 > [邮件触发器(IMAP)](Activities/Triggers/IMAPTrigger.md)**：用于监听支持 IMAP 协议的邮箱接收新邮件事件，设置特定触发条件，满足条件时自动执行流程。
2. **代码工具 > JSON > [序列化](Activities/CodeExecuter/JSON/SerializeObject.md)**：可将 .NET 对象序列化为 JSON 字符串。
3. **代码工具 > JSON > [反序列化](Activities/CodeExecuter/JSON/DeserializeObject.md)**：可将 JSON 字符串反序列化为 .NET 对象。
4. **软件自动化 > Office Excel > [刷新透视表](Activities/AppAutomation/OfficeExcel/RefreshPivotTable.md)**：实现刷新指定透视表的数据。
5. **软件自动化 > Office Excel > [创建透视表](Activities/AppAutomation/OfficeExcel/CreatePivotTable.md)**：实现在 Excel 中创建透视表。
6. **代码工具 > HTTP > [HTTP请求](Activities/CodeExecuter/HTTP/HTTPRequest.md)**：实现发送 HTTP 请求并返回响应的数据，并支持测试配置的 HTTP 请求是否可用。

#### 【小程序】
关于小程序的详情，请参见 [关于云扩工作台](Apps/aboutApps.md)。

1. 新增顶部导航、左侧导航组件，支持应用内多页面跳转。
2. 新增流程组件，支持一键启动控制台流程。
3. 支持应用版本管理，控制台统一对应用进行上下架及版本管理。
4. 支持**我的应用**查找并运行。

#### 【控制台】
   
1. 对控制台整体架构进行升级，同时丰富RPA调度功能，上线云端版和私有化版，支持功能包括 [调度队列](Console/queue/aboutqueue.md)、[任务记录](Console/job/aboutJob.md)、 [文档理解](Console/docreader/aboutDocreader.md)、[资产管理](Console/datacentor/asset/AboutAsset.md)。

### 改进与增强

#### 【编辑器】
1. 更换安装框架，优化安装/升级体验，解决了由杀毒软件导致的安装失败问题。
2. 非管理员权限运行编辑器时，元素识别时高亮外层窗体，并在点击时提示。
3. 选择器编辑器中 Java 应用的 Name 属性全部层级支持通配符。
4. 选择器编辑器界面优化，使得用户操作体验更友好。
5. 界面自动化组件支持即刻优雅终止流程。

#### 【组件】
1. 界面自动化下的组件全部新增超时属性。
2. **获取含 OCR 文本的元素**、**判断 OCR 文本是否存在**组件的文本属性支持正则表达式。
3. 优化钉钉程序内元素识别，使得录制技术 UIA 可识别大部分元素。
#### 【机器人】
优化安装/升级体验。

## 2020.08.31 发版说明

2020.08.31 发布了云扩 RPA 编辑器和机器人，本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2008.12 |
| 机器人   | 1.1.2008.12 |

你可以通过[云扩控制台](https://console.encoo.com/)下载并体验相关产品。

### 新增功能

#### 【编辑器】

1. 支持**大纲**层级显示，用于显示当前流程的结构，可快速定位对应组件。
2. 当光标置于属性输入框内时，鼠标右键可快速打开**表达式编辑器**菜单，对变量、参数或表达式进行操作。
3. 新增全局快捷键 **Ctrl+Alt+F5**，使编辑器最小化后在后台运行时，也能够停止执行流程。
4. 暂停调试支持在任意时刻快速暂停调试过程。暂停时，正在调试的组件将高亮显示。

#### 【组件】

1. **系统 > [提示框](Activities/System/PromptBox.md)**：用于在 Windows 桌面右下角展示在流程中必要的提示信息。
2. **软件自动化 > Office Excel > [ 重置密码](Activities/AppAutomation/OfficeExcel/OfficeExcelResetPassword.md)**：在**打开/新建**组件中使用，对 Excel 文件进行增加、更新或清除密码。

#### 【机器人】

1. 在**设置**页面中新增[关于页](Robot/Settings/About.md)，可查看软件版本、许可证有效期及更改激活方式。
2. 新增[正在执行](Robot/RunningProcess.md)页面，可以查看正在执行的流程相关信息。
3. 在执行流程时，支持权限配置。具体功能请参见[流程库](Robot/localworkflow.md)。

### 改进与增强

#### 【编辑器】
1. 优化项目打开速度，较之前更快，提升用户体验。
2. 优化复制粘贴组件速度，较之前更快，提升用户体验。
3. 项目运行或调试过程中，输出面板对当前过程进行提示，使用户更加明确当前执行过程。

## 2020.08.13 发版说明

2020.08.13 发布了云扩 RPA 编辑器和机器人，本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2008.5 |
| 机器人   | 1.1.2008.5 |


你可以通过[云扩控制台](https://console.encoo.com/)下载并体验相关产品。

### 新增功能

#### 【编辑器】

1. 流程编辑过程中，通过右键组件可选择禁用或启用组件。运行或调试时，禁用的组件将会被忽略执行。
2. 在主界面菜单栏中新增**意见反馈**按钮，可快速寻求帮助。
3. 输出面板支持分类筛选输出信息，包括**错误**、**信息**、**调试**这三类，用于分类查看日志信息。


#### 【组件】

1. **界面自动化 > [匹配图片](Activities/UIAutomation/MatchImage.md)**：实现在指定范围内寻找指定图片，返回符合的结果集。
1. **界面自动化 > [设置焦点](Activities/UIAutomation/SetFocus.md)**：实现为指定元素设置焦点，支持桌面端和浏览器端。
1. **界面自动化 > [选择多个项目](Activities/UIAutomation/SelectMultipleItems.md)**：实现多个项目的同时选择，此组件仅当原页面支持多选时生效。
1. **界面自动化 > [高亮](Activities/UIAutomation/Highlight.md)**：实现指定元素高亮，可选择颜色和时间。
1. **界面自动化 > [等待元素属性值](Activities/UIAutomation/WaitElementAttributeValue.md)**：实现等待指定元素的属性值为指定值时，才执行下一个组件，否则会在超时时间范围内一直等待。
1. **界面自动化 > [获取元素属性值](Activities/UIAutomation/GetElementAttributeValue.md)**：实现获取指定元素的属性值，并将其存储在输出变量属性值中。
1. **界面自动化 > OCR > [获取 OCR 文本](Activities/UIAutomation/OCR/GetOCRText.md)（企业版）**：实现对指定元素或图片进行 OCR 并返回结果。
1. **界面自动化 > OCR > [获取含 OCR 文本的元素](Activities/UIAutomation/OCR/GetSpecificTextOCRElement.md)（企业版）**:实现对指定元素或图片进行 OCR ，并查找包含指定文本的元素，将其存储在输出属性 OCR 元素内。
1. **界面自动化 > OCR > [判断 OCR 文本是否存在](Activities/UIAutomation/OCR/IdentifyOCRTextExist.md)（企业版）**：实现对指定元素或图片进行 OCR ，并判断指定文本是否存在，将其结果存储在输出属性 OCR 元素内。
2. **软件自动化 > 邮件**：[获取邮件(Exchange)](Activities/AppAutomation/Mail/GetExchangeMail.md) 、 [发送邮件(Exchange)](Activities/AppAutomation/Mail/SendExchangeMail.md)
3. **代码工具 > 文本处理**: [验证文本有效性](Activities/CodeExecuter/TextProcessing/VerifyTextActivity.md)、[提取文本](Activities/CodeExecuter/TextProcessing/ExtractTextActivity.md)、 [替换文本](Activities/CodeExecuter/TextProcessing/ReplaceTextActivity.md)、[截取文本](Activities/CodeExecuter/TextProcessing/GetSubstringActivity.md)、[获取文本长度](Activities/CodeExecuter/TextProcessing/GetLengthOfTextActivity.md)、[获取文本索引](Activities/CodeExecuter/TextProcessing/GetIndexOfTextActivity.md)
4. **流程控制 > [赋值（多个） ](Activities/WorkflowControl/MultipleAssign.md)**
5. **软件自动化 > Office Excel > [插入图片](Activities/AppAutomation/OfficeExcel/InsertPicture.md)**：实现指定单元格插入图片。
6. **流程控制 > 判断 > [条件( Switch )](Activities/WorkflowControl/Determine/Switch.md)**：实现指定 C# 表达式，并根据每个 Case 判断执行符合条件的流程。
7. **系统 > 文件 > [遍历文件夹](Activities/System/File/ForeachFolder.md)**
8. **代码工具 > 集合处理** ：[对象是否存在](Activities/CodeExecuter/CollectionProcessing/ExistsInCollectionActivity.md)、[添加对象](Activities/CodeExecuter/CollectionProcessing/AddToCollectionActivity.md)、[清空对象](Activities/CodeExecuter/CollectionProcessing/ClearCollectionActivity.md)、[移除对象](Activities/CodeExecuter/CollectionProcessing/RemoveFromCollectionActivity.md)、[获取集合长度](Activities/CodeExecuter/CollectionProcessing/GetLengthOfCollectionActivity.md)、[初始化集合](Activities/CodeExecuter/CollectionProcessing/InitializeCollectionActivity.md)

#### 【机器人】

1. 新增机器人[概览页](Robot/Overview.md)，可展示当前机器人全局数据。
1. 新增[流程执行历史页](Robot/ProcessHistory.md)，可展示流程执行的历史记录。
1. 新增**设置 > 基本**页面，可[配置日志与视频文件保留时间](Robot/Settings/Basic.md)。

### 改进与增强

#### 【编辑器】
1. 发布项目前，对项目的正确性进行校验。
2. 将部分弹窗更改为浮窗，提升用户体验。
#### 【组件】
提升[调用流程](Activities/WorkflowControl/InvokeWorkflow.md)组件体验，点击**导入参数**可直接将子流程参数导入。
#### 【自动化驱动】
1. 加强对用友 NC 系列软件的支持。
2. 支持在金蝶 EAS 系列软件中，对报表类型界面通过**获取结构化数据**获取报表数据。
3. 在图像识别模式下，**等待元素出现**组件返回的控件元素为图象，而非锚点。
4. 支持内嵌IE浏览器中元素的识别。
5. 支持360安全浏览器兼容模式下元素的识别。
6. 浏览器端支持**图像识别**功能。
7. 对于桌面应用，**输入文本**组件支持**清空文本**操作。
8. **获取区域文本**组件更名为 **获取区域结构**（企业版）。
9. **悬停**组件支持图像识别。



## 2020.07.17 发版说明

2020.07.17 发布了云扩 RPA 编辑器和机器人社区版，本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2007.29 |
| 机器人   | 1.1.2007.29 |


你可以通过云扩 RPA 控制台 -> [安装包下载](https://console.encoo.com/#/download) 页面体验相关产品。

### 新增功能

#### 【编辑器】
1. 支持在表达式编辑器中，选中变量名，使用 **Ctrl+B** 快捷键快速创建变量。
2. 针对含有多个 xaml 文件的复杂流程，支持通过[调试/运行文件](Studio\process\Debugging\partialDebug.md)来进行分布调试。
3. 支持使用编辑器直接发布自动化项目到本地机器人，实现无缝对接。
4. 在编辑器右下角支持浮窗通知，针对编辑器更新、部分项目操作反馈进行提醒，降低了弹窗通知带来的干扰率，提升用户体验。
5. 集成 NuGet 开源项目，可以方便的引用 NuGet 应用。
6. 支持使用元素探测器选择元素，功能较此前的选择器编辑器更强，此功能仅在企业版中支持，可参见[元素探测器](Activities/Appendix/UiDetector.md)。
7. 在项目设置中，支持设置组件的延迟和超时属性，支持配置默认浏览器属性，可参见[项目设置](Studio/process/ProjectSettings.md)。
   

#### 【组件】
1. **流程控制 > [状态机](Activities/WorkflowControl/StateMachine/StateMachine.md)**：实现基于状态机范例的工作流程。
2. **代码工具 > 数据处理 > [数据格式化](Activities/CodeExecuter/DataProcessing/FormatData.md)**：可实现对输入数据按照数值、日期和时间、货币和百分比进行格式化。
3. **流程控制**：[重试](Activities/WorkflowControl/Retry.md)、[抛出异常](Activities/WorkflowControl/Throw.md)、[重新抛出异常](Activities/WorkflowControl/ReThrow.md)。
4. **系统 > [下拉选择框](Activities/System/DropdownListDialog.md)**：方便在流程中弹出下拉选择框形态的用户交互界面。
5. **数据表 > [追加到CSV文件](Activities/DataTable/AppendToCSV.md)**：实现将数据表追加到已有 CSV 文件。
6. **软件自动化 > 邮件**：[获取邮件(Outlook)](Activities/AppAutomation/Mail/GetOutlookMail.md)、[发送邮件(Outlook)](Activities/AppAutomation/Mail/SendOutlookMail.md)。
7. **界面自动化 > 桌面控件专有**：[获取焦点控件](Activities/UIAutomation/DesktopOnly/GetFocus.md)、[切换控件](Activities/UIAutomation/DesktopOnly/SwitchControl.md)，这两个控件仅在企业版中支持。

### 改进与增强

#### 【编辑器】
1. 支持新增序列或流程图作为子流程。
2. 导出项目时，支持导出后选择是否打开所在文件夹。
3. 导入项目时，支持导入后选择是否立即打开该项目。
4. 统一项目名称及流程包名称的命名规则，避免发布流程时名称校验不通过。
5. 支持 Java 扩展。你可以使用 Java 扩展识别一些原本无法识别的桌面 Java 应用中的元素。
   
#### 【组件】
1. [发送邮件(SMTP)](Activities/AppAutomation/Mail/SendMailSMTP.md)、[获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md)、[获取邮件(POP3)](Activities/AppAutomation/Mail/GetMailPOP3.md)组件支持手动选择安全方式。
2. [获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md)组件支持仅获取未读邮件。



## 2020.06.16 发版说明

2020.06.16 发布了云扩 RPA 编辑器和机器人社区版，本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2006.16 |
| 机器人   | 1.1.2006.16 |

你可以通过云扩 RPA 控制台 -> [安装包下载](https://console.encoo.com/#/download) 页面体验相关产品。

### 新增功能

#### 【编辑器】
1. 调试过程中，支持在[变量面板](Studio\process\Debugging\ValuePanel.md)查看每一个变量在当前组件的类型和值，以此我们可以来判断流程是否正确执行，且可帮助定位流程错误位置。
2. 新建项目时，支持根据当前录制的桌面应用选择对应录制技术：UIA3 或 UIA 。
3. 在导入列表处，支持删除未使用或报错的[命名空间](Studio\process\developProject\ImportNamespaces.md)。
4. 项目运行时，支持最小化编辑器主界面，降低对界面自动化项目运行的干扰率。
5. 支持更多的快捷键，参见[键盘快捷键](Studio/quickStart/KeyboardShortcuts.md)，使用户使用更便捷。
6. 界面自动化 > 支持360安全浏览器。新增浏览器的支持类型，使您可以操作360安全浏览器。
#### 【组件】
1. **界面自动化 > SAP** ：[登录应用](Activities/UIAutomation/SAP/SAP_Login.md)、[获取状态栏信息](Activities/UIAutomation/SAP/SAP_GetStatus.md)、[选择日期](Activities/UIAutomation/SAP/SAP_SelectCalendar.md)、[选择 SAP 项](Activities/UIAutomation/SAP/SAP_Select.md)、[执行事务](Activities/UIAutomation/SAP/SAP_Transaction.md)，仅在企业版中支持这些组件。
2. **界面自动化 > [截屏](Activities/UIAutomation/Screenshot.md)**。
3. **系统 > [设置日期和时间](Activities/System/SetDateTime.md)**：实现指定日期和时间并输出DateTime类型结果。
4. **系统**：[选择文件](Activities/System/File/SelectFile.md)、[选择文件夹](Activities/System/File/SelectFolder.md)。
5. **软件自动化 > Office Excel > [设置文字颜色](Activities/AppAutomation/OfficeExcel/SetTextColor.md)** ：使用拾色器提升颜色设置体验。

#### 【机器人】
执行本地流程时支持填写流程参数，详见[执行本地流程](Robot/localworkflow.md)。

### 改进与增强

#### 【编辑器】
1. 日志输出界面优化，由左侧显示更改为编辑器底部显示，使之更全局化，提升用户体验。
2. 支持更详细的项目打开及编译错误描述，更易定位错误位置。

#### 【组件】
1. 优化**软件自动化 > Office Excel > [排序](Activities/AppAutomation/OfficeExcel/Sort.md)** 组件，支持指定开始行号。
2. 优化**软件自动化 > Office Excel > [设置单元格背景色](Activities/AppAutomation/OfficeExcel/SetCellBackcolor.md)** 组件，使用拾色器提升颜色设置体验。


#### 【自动化场景】
1. 增强对用友 NC 系列软件和金蝶 EAS 系列软件的支持。
2. 增强桌面录制技术 UIA3 识别微信，实现获取文本、选择项目时可以自动滚动联系人列表操作。
3. 增强 JAVA 应用在不同分辨率 DPI 下的识别回放。
4. **点击**组件新增辅助键属性。如，你可以在点击的同时按下 **Ctrl** 键。

## 2020.05.21 发版说明

2020.05.21 发布了云扩 RPA 编辑器和机器人社区版，本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2005.3 |
| 机器人   | 1.1.2005.3 |

你可以通过云扩 RPA 控制台 -> [安装包下载](https://console.encoo.com/#/download) 页面体验相关产品。

### 新增功能
#### 【组件】
1. **软件自动化 > 邮件 > [获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md?_v=v2020.4)**。
1. **软件自动化 > Office Excel > [自动填充](Activities/AppAutomation/OfficeExcel/AutoFillRange.md?_v=v2020.4)**。
2. **系统 > [设置剪贴板文本](Activities/System/SetContentsToClipboard.md?_v=v2020.4)**：实现设置文本内容到剪贴板。
   

#### 【组件市场】
1. 在**组件市场**中新增[Office PowerPoint组件包](https://marketplace.encoo.com/#/activity/detail?packageId=Encootech.OfficePPT)，实现对PPT常用功能的支持。
2. 在**组件市场**中新增[竹间智能语音识别](https://marketplace.encoo.com/#/activity/detail?packageId=Emotibot)，实现语音转文字功能 。
#### 【编辑器】
支持将流程中的组件保存为子流程文件，你可以使用本功能将复杂流程拆解为多个简单的流程。

### 改进与增强
#### 【组件】
提升 **软件自动化 > Office Excel** 系列组件执行性能。
#### 【编辑器】
1. 增强**表达式编辑器**的**智能感知**功能，支持变量/参数/方法名称联想。
2. 针对社区版许可证超出配额的情况，增加解决方法的提示。
3. 在创建变量/参数时，支持快速创建 DataTable / IUiObject 类型的变量/参数。
4. 支持通过组件的右键菜单来访问组件的帮助文档。

### 问题修复

#### 【编辑器】
1. 修复了表达式编辑时，自动补入变量名不齐全的问题。
2. 修复了调试时不能查看容器类组件中最后一个组件的属性的问题。
3. 修复了搜索组件时，搜索结果展示不全的问题。
4. 修复了修改变量值后，调试项目时，修改不生效的问题。
5. 修复了编辑器界面偶尔无法点击的问题。
