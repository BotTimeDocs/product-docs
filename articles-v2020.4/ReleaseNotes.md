# 云扩产品发版说明





### 新增功能

### 组件

1.  PDF操作：[合并文件](Activities/AppAutomation/PDF/MergePDF.md)、[提取为新文档](Activities/AppAutomation/PDF/ExtractToNewFile.md)、[获取页数](Activities/AppAutomation/PDF/GetPageNumbers.md)、[读取图片](Activities/AppAutomation/PDF/ExtractImages.md)、[读取文本](Activities/AppAutomation/PDF/ExtractText.md)
1.  系统：[重命名文件或文件夹](Activities/System/File/RenameFileOrFolder.md)、[输入密码](Activities/System/InputPasswordDialogActivity.md)
1.  控制台交互：[文档理解](Activities/Console/DocReader.md)、[获取资产](Activities/Console/GetAssets.md)
1.  数组操作：[初始化数组](Activities/CodeExecuter/数组处理/InitializeArrayActivity.md)、[元素是否存在](Activities/CodeExecuter/数组处理/ExistsInArrayActivity.md)、[获取数组长度](Activities/CodeExecuter/数组处理/GetLengthOfArrayActivity.md)
1.  HTTP: [下载文件](Activities/CodeExecuter/HTTP/HTTPDownload.md)

### 机器人

1. 新增[定时任务](Robot/CronJob.md)功能
1. 新增集成[云扩流程市场](Robot/ProcessMarket.md)


### 增强功能

1. 【组件】[文件触发器](Activities/Triggers/FileTrigger.md)增加输出监听的文件路径
1. 【组件】[邮件触发器(IMAP)](Activities/Triggers/IMAPTrigger.md)、[邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md)和[邮件触发器(Exchange)](Activities/Triggers/ExchangeTrigger.md) 增加输出监听到的邮件
1. 【组件】[获取末列号](Activities/AppAutomation/OfficeExcel/GetLastColumn.md)增加输出字母和数字列号
















## 2020.10.19 发版说明
2020.10.19 发布了云扩 RPA 编辑器。
本次发布的产品版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2010.8 |

你可以通过[*云扩控制台*](https://console.encoo.com/) 下载并体验相关产品。
### 新增功能

#### 【编辑器】
1. 在新建组件项目时将多个可重复使用的流程封装为组件包。
2. 从模板新建自动化项目。
3. 支持查看和编辑控制台的流程。
4. 支持从最近列表打开最近使用的项目。
5. 支持关闭当前打开的项目。
6. 在项目中支持创建子文件夹存放文件。
7. 在项目中支持对项目属性进行设置。
8. 在项目中支持新增状态机作为子流程。
9. 调试状态下支持忽略、重试、重启。
10. 通过快捷键Ctrl+E快速打开表达式编辑器。


### 增强功能
1. 【编辑器】优化**开始**页面的界面布局。
2. 【编辑器】优化调整**流程市场**、**组件**等应用的入口位置。
3. 【编辑器】优化在线咨询及增加在线咨询入口。


## 2020.09.27 发版说明

2020.09.27 发布了云扩 RPA 编辑器、机器人和工作台。
本次发布的产品版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2009.11 |
| 机器人   | 1.1.2009.11 |
| 工作台   | V1.0.0 |

你可以通过[*云扩控制台*](https://console.encoo.com/) 下载并体验编辑器和机器人，或者申请体验工作台产品。

### 新增功能

#### 【编辑器】

1. Microsoft Edge 支持。自动化 Edge 操作之前，请先安装 [Microsoft Edge 扩展](Studio\Extensions\EdgeExtension.md)。
2. 选择器编辑器新增获取 XPath 功能。参看[选择器](Activities\Appendix\Selector.md)。
3. IE 前端日志收集器程序。参看[收集 IE 前端日志工具](Activities\Appendix\IELog.md)。

#### 【组件】

1. [文件触发器](Activities/Triggers/FileTrigger.md)
1. [邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md)
1. [邮件触发器(Exchange)](Activities/Triggers/ExchangeTrigger.md)
1. [邮件触发器(IMAP)](Activities/Triggers/IMAPTrigger.md)
1. [JSON - 序列化](Activities/CodeExecuter/JSON/SerializeObject.md)
1. [JSON - 反序列化](Activities/CodeExecuter/JSON/DeserializeObject.md)
1. [Excel - 刷新透视表](Activities/AppAutomation/OfficeExcel/RefreshPivotTable.md)
1. [Excel - 创建透视表](Activities/AppAutomation/OfficeExcel/CreatePivotTable.md)
1. [HTTP - HTTP请求](Activities/CodeExecuter/HTTP/HTTPRequest.md)

#### 【工作台】
关于工作台的详情，请参考 [关于云扩工作台](Apps/aboutApps.md)。

1. 支持创建多页面应用。
2. 支持通过应用调用流程。
3. 支持应用发布到控制台。
4. 支持*我的应用*查找并运行。

#### 【控制台】

1. 和工作台的通信，对应用的管理：
    1. 支持查看发布的应用；
    2. 支持应用上下架。
2. 整体架构升级，上线云端版和私有化版，支持功能包括：
    1. 调度队列，通过机器人集群实现对流程任务动态分配；
    2. 任务记录，展示所有流程任务的执行记录及日志详情；
    3. 文档理解，用于配置各类模板实现对电子版PDF非结构化信息抽取；
    4. 资产管理，定义各类参数及账户密码凭证供流程进行调用。

### 增强功能

1. 【编辑器】优化安装/升级体验，更换安装框架
2. 【编辑器】非管理员权限运行编辑器时，元素识别时高亮外层窗体，并在点击时提示
8. 【编辑器】选择器编辑器Java应用的Name属性全部层级支持通配符
4. 【编辑器】选择器编辑器界面优化
5. 【编辑器】界面自动化组件支持即刻优雅终止流程
6. 【组件】界面自动化下组件全部新增超时属性
7. 【组件】*获取含OCR文本元素*，*判断OCR文本是否存在*组件的文本属性支持正则表达式
3. 【组件】优化钉钉程序内元素识别
1. 【机器人】优化安装/升级体验

## 2020.08.31 发版说明

2020.08.31 发布了云扩 RPA 编辑器和机器人。
本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2008.12 |
| 机器人   | 1.1.2008.12 |

你可以通过[*云扩控制台*](https://console.encoo.com/) 下载并体验相关产品。

### 新增功能

#### 【编辑器】

1. 支持大纲，用于显示当前流程的结构，可快速定位应组件。
2. 表达式编辑器支持右键菜单。
3. 新增全局快捷键 *Ctrl+Alt+F5*，使编辑器最小化后在后台运行时,也能够停止执行流程。
4. 调试状态下，支持暂停调试过程。

#### 【组件】

1. [提示框](Activities/System/PromptBox.md)。
1. [Excel 组件 - 重置密码](Activities/AppAutomation/OfficeExcel/OfficeExcelResetPassword.md)。

#### 【机器人】

1. [关于页](Robot/Settings/About.md)。
1. 新增[正在执行](Robot/RunningProcess.md)页面，可以查看正在执行的流程相关信息。
1. 在执行流程时，支持权限配置。具体功能请参看[流程库](Robot/localworkflow.md)。

### 增强功能

1. 【编辑器】项目操作性能优化，优化如下：
   - 项目打开速度；
   - 复制粘贴组件速度；
   - 运行/调试时增加提示信息。

## 2020.08.13 发版说明

2020.08.13 发布了云扩 RPA 编辑器和机器人。
本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2008.5 |
| 机器人   | 1.1.2008.5 |


你可以通过[*云扩控制台*](https://console.encoo.com/) 下载并体验相关产品。

### 新增功能

#### 【编辑器】

1. 支持启用/禁用组件。
2. 新增意见反馈按钮，可快速寻求帮助。
3. 输出面板支持分类筛选输出信息，信息有以下分类：
    - 错误；
    - 信息；
    - 调试。

#### 【组件】

1. [匹配图片](Activities/UIAutomation/MatchImage.md)
1. [设置焦点](Activities/UIAutomation/SetFocus.md)
1. [选择多个项目](Activities/UIAutomation/SelectMultipleItems.md)
1. [高亮](Activities/UIAutomation/Highlight.md)
1. [等待元素属性值](Activities/UIAutomation/WaitElementAttributeValue.md)
1. [获取元素属性值](Activities/UIAutomation/GetElementAttributeValue.md)
1. [获取OCR文本](Activities/UIAutomation/OCR/GetOCRText.md)【企业版】
1. [获取含OCR文本的元素](Activities/UIAutomation/OCR/GetSpecificTextOCRElement.md)【企业版】
1. [判断OCR文本是否存在](Activities/UIAutomation/OCR/IdentifyOCRTextExist.md)【企业版】
1. [获取邮件(Exchange)](Activities/AppAutomation/Mail/GetExchangeMail.md) 与 [发送邮件(Exchange)](Activities/AppAutomation/Mail/SendExchangeMail.md)
1. 6个文本处理类组件，分别为:
    - [验证文本有效性](Activities/CodeExecuter/TextProcessing/VerifyTextActivity.md)
    - [提取文本](Activities/CodeExecuter/TextProcessing/ExtractTextActivity.md)
    - [替换文本](Activities/CodeExecuter/TextProcessing/ReplaceTextActivity.md)
    - [截取文本](Activities/CodeExecuter/TextProcessing/GetSubstringActivity.md)
    - [获取文本长度](Activities/CodeExecuter/TextProcessing/GetLengthOfTextActivity.md)
    - [获取文本索引](Activities/CodeExecuter/TextProcessing/GetIndexOfTextActivity.md)
1. [多赋值](Activities/WorkflowControl/MultipleAssign.md)
1. [Office Excel -> 插入图片](Activities/AppAutomation/OfficeExcel/InsertPicture.md)
1. [条件(Switch)](Activities/WorkflowControl/Determine/Switch.md)
1. [遍历文件夹](Activities/System/File/ForeachFolder.md)
1. 6个集合处理类组件，分别为:
    - [对象是否存在](Activities/CodeExecuter/CollectionProcessing/ExistsInCollectionActivity.md)
    - [添加对象](Activities/CodeExecuter/CollectionProcessing/AddToCollectionActivity.md)
    - [清空对象](Activities/CodeExecuter/CollectionProcessing/ClearCollectionActivity.md)
    - [移除对象](Activities/CodeExecuter/CollectionProcessing/RemoveFromCollectionActivity.md)
    - [获取集合长度](Activities/CodeExecuter/CollectionProcessing/GetLengthOfCollectionActivity.md)
    - [初始化集合](Activities/CodeExecuter/CollectionProcessing/InitializeCollectionActivity.md)

#### 【机器人】

1. [概览页](Robot/Overview.md)
1. [流程执行历史页](Robot/ProcessHistory.md)
1. [配置日志与视频文件保留时间](Robot/Settings/Basic.md)

### 增强功能

1. 【编辑器】发布项目前，对项目的正确性进行校验。
2. 【编辑器】将部分弹窗更改为浮窗，提升用户体验。
3. 【组件】提升[调用流程](Activities/WorkflowControl/InvokeWorkflow.md)组件体验，点击*导入参数*可直接将子流程参数导入。
4. 【自动化驱动】加强对 NC 的支持。
5. 【自动化驱动】支持在 EAS 中，在报表类型界面通过*获取结构化数据*获取报表数据。
6. 【自动化驱动】在图像识别模式下，*等待元素出现*组件返回的控件元素为图象，而非锚点。
7. 【自动化驱动】支持内嵌IE浏览器中元素的识别。
1. 【自动化驱动】支持360安全浏览器兼容模式下元素的识别。
8. 【自动化驱动】浏览器端支持*图像识别*功能。
9. 【自动化驱动】对于桌面应用，*输入文本*组件支持*清空文本*操作。
10. 【自动化驱动】*获取区域文本* 组件更名为 *获取区域结构*。【企业版】
11. 【自动化驱动】悬停组件支持图像识别。



## 2020.07.17 发版说明

2020.07.17 发布了云扩 RPA 编辑器和机器人社区版。
本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2007.29 |
| 机器人   | 1.1.2007.29 |


你可以通过*云扩 RPA 控制台* -> [*安装包下载*](https://console.encoo.com/#/download) 页面体验相关产品。

### 新增功能

1. 【编辑器】支持在表达式编辑器中，选中变量名，使用 **Ctrl+B** 快捷键快速创建变量。
2. 【编辑器】支持单独调试或运行 .xaml 流程文件。
3. 【编辑器】支持使用编辑器直接发布自动化项目到本地机器人。
4. 【编辑器】编辑器右下角支持浮窗通知。
5. 【编辑器】集成 NuGet，可以方便的引用 NuGet 应用。
1. 【编辑器】支持使用元素探测器选择元素，功能较此前的选择器编辑器更强。此功能仅在企业版中支持。参见[元素探测器](Activities/Appendix/UiDetector.md)。
1. 【编辑器】在项目设置中，支持设置组件的延迟和超时属性，支持配置默认浏览器属性。参见[项目设置](Studio/process/ProjectSettings.md)。
1. 【组件】新增 **状态机** 系列组件。详情请查看[状态机](Activities/WorkflowControl/StateMachine/StateMachine.md)。
1. 【组件】新增 **数据格式化** 组件。详情请查看[数据格式化](Activities/CodeExecuter/DataProcessing/FormatData.md)。
1. 【组件】新增流程控制类组件：**重试**、**抛出异常**和**重新抛出异常**。详情请查看[重试](Activities/WorkflowControl/Retry.md)、[抛出异常](Activities/WorkflowControl/Throw.md)、[重新抛出异常](Activities/WorkflowControl/ReThrow.md)。
1. 【组件】新增 **下拉选择框** 组件，方便在流程中弹出下拉选择框形态的用户交互界面。详情请查看[下拉选择框](Activities/System/DropdownListDialog.md)。
1. 【组件】新增 **追加到CSV文件** 组件。详情请查看[追加到CSV文件](Activities/DataTable/AppendToCSV.md)。
1. 【组件】新增 **获取邮件(Outlook)**、**发送邮件(Outlook)**。你可以使用本地 Outlook 发送和获取邮件。详情请查看[获取邮件(Outlook)](Activities/AppAutomation/Mail/GetOutlookMail.md)、[发送邮件(Outlook)](Activities/AppAutomation/Mail/SendOutlookMail.md)。
1. 【组件】新增 **获取焦点控件**，**切换控件**。这两个空间仅在企业版中支持。参见[获取焦点控件](Activities/UIAutomation/DesktopOnly/GetFocus.md)和[切换控件](Activities/UIAutomation/DesktopOnly/SwitchControl.md)。

### 增强功能

1. 【编辑器】支持新增序列或流程图作为子流程。
2. 【编辑器】导出项目时，支持导出后选择是否打开所在文件夹。
3. 【编辑器】导入项目时，支持导入后选择是否立即打开该项目。
4. 【编辑器】统一项目名称及流程包名称的命名规则，避免发布流程时名称校验不通过。
1. 【组件】**发送邮件(SMTP)**、**获取邮件(IMAP)**、**获取邮件(POP3)** 组件支持手动选择安全方式。详情请查看[发送邮件(SMTP)](Activities/AppAutomation/Mail/SendMailSMTP.md)、[获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md)、[获取邮件(POP3)](Activities/AppAutomation/Mail/GetMailPOP3.md)。
1. 【组件】**获取邮件(IMAP)** 组件支持仅获取未读邮件。详情请查看[获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md)。
1. 【机器人】UI 体验优化。
1. 【编辑器】支持 Java 扩展。你可以使用 Java 扩展识别一些原本无法识别的桌面 Java 应用中的元素。

## 2020.06.16 发版说明

2020.06.16 发布了云扩 RPA 编辑器和机器人社区版。
本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2006.16 |
| 机器人   | 1.1.2006.16 |

你可以通过*云扩 RPA 控制台* -> [*安装包下载*](https://console.encoo.com/#/download) 页面体验相关产品。

### 新增功能

1. 【编辑器】调试时，在变量面板支持查看值的详细信息。
2. 【编辑器】新建项目时支持选择桌面录制技术 UIA/UIA3。
3. 【编辑器】支持删除命名空间。
4. 【编辑器】支持设置运行时是否最小化编辑器主界面。
5. 【编辑器】支持更多的快捷键。详情请参看[键盘快捷键](Studio/quickStart/KeyboardShortcuts.md)。
6. 【插件】支持360安全浏览器。
9. 【组件】企业版编辑器中包含 SAP 相关组件：[登录应用](Activities/UIAutomation/SAP/SAP_Login.md)，[获取状态栏信息](Activities/UIAutomation/SAP/SAP_GetStatus.md)，[选择日期](Activities/UIAutomation/SAP/SAP_SelectCalendar.md)，[选择SAP项](Activities/UIAutomation/SAP/SAP_Select.md)，[执行事务](Activities/UIAutomation/SAP/SAP_Transaction.md)。
1. 【组件】新增“截屏”组件。详情请查看[截屏](Activities/UIAutomation/Screenshot.md)。
6. 【组件】新增“设置日期和时间”组件。详情请查看[设置日期和时间](Activities/System/SetDateTime.md)。
7. 【组件】新增“选择文件”及“选择文件夹”对话框组件。详情请查看[选择文件](Activities/System/File/SelectFile.md)与[选择文件夹](Activities/System/File/SelectFolder.md)。
8. 【组件】新增 Office Excel "设置文字颜色"组件并使用拾色器提升颜色设置体验。详情请查看[设置文字颜色](Activities/AppAutomation/OfficeExcel/SetTextColor.md)。
9. 【机器人】执行本地流程时支持填写流程参数。

### 增强功能

1. 【编辑器】输出面板改造等界面优化。
1. 【编辑器】更详细的项目打开及编译错误描述，更易定位错误位置。
1. 【组件】优化 Office Excel “排序”组件：支持指定开始行号。详情请查看[排序](Activities/AppAutomation/OfficeExcel/Sort.md)。
1. 【组件】优化 Office Excel “设置单元格背景色”组件：使用拾色器提升颜色设置体验。详情请查看[设置单元格背景色](Activities/AppAutomation/OfficeExcel/SetCellBackcolor.md)。
1. 【自动化场景】增强对用友 NC 和金蝶 EAS 的支持。
1. 【自动化场景】增强 UIA3 识别微信。
1. 【自动化场景】增强 JAVA 应用在不同 DPI 下的识别回放。
1. 【自动化场景】点击组件新增辅助键属性。比如，你可以在点击的同时按下 *Ctrl* 键。

## 2020.05.21 发版说明

2020.05.21 发布了云扩 RPA 编辑器和机器人社区版。
本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2005.3 |
| 机器人   | 1.1.2005.3 |

你可以通过*云扩 RPA 控制台* -> [*安装包下载*](https://console.encoo.com/#/download) 页面体验相关产品。

### 新增功能
1. 【组件】新增邮件相关的组件“获取邮件(IMAP)”。详情请参看 [获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md?_v=v2020.4)。
2. 【组件】新增 Office Excel 相关的组件“自动填充”。详情请参看 [自动填充](Activities/AppAutomation/OfficeExcel/AutoFillRange.md?_v=v2020.4)。
3. 【组件】新增剪贴板相关的组件“设置剪贴板文本”。详情请参看 [设置剪贴板文本](Activities/System/SetContentsToClipboard.md?_v=v2020.4) 。
4. 【组件市场】新增对 Office PowerPoint 支持的组件包。详情请查看[OfficePPT组件包](https://marketplace.encoo.com/#/activity/detail?packageId=Encootech.OfficePPT)。
5. 【组件市场】新增语音识别组件包。详情请查看[竹间智能语音识别](https://marketplace.encoo.com/#/activity/detail?packageId=Emotibot) 。
6. 【编辑器】支持将流程中的组件保存为子流程文件。你可以使用本功能将复杂流程拆解为多个简单的流程。

### 增强功能
1. 【组件】提升 Office Excel 组件执行性能。
1. 【机器人】增强机器人执行稳定性。
1. 【编辑器】增强了表达式编辑器的智能感知功能，支持变量/参数/方法名称联想。
1. 【编辑器】针对社区版许可证超出配额的情况，增加解决方法的提示。
1. 【编辑器】在创建变量/参数时，支持快速创建 DataTable / IUiObject 类型的变量/参数。
1. 【编辑器】支持通过组件的右键菜单，访问组件的帮助文档。

### 修复问题

1. 【编辑器】修复了表达式编辑时，自动补入变量名不齐全的问题。
1. 【编辑器】修复了调试时不能查看容器类组件中最后一个组件的属性的问题。
1. 【编辑器】修复了搜索组件时，搜索结果展示不全的问题。
1. 【编辑器】修复了修改变量值后，调试项目时，修改不生效的问题。
1. 【编辑器】修复了编辑器界面偶尔无法点击的问题。
