# 云扩 RPA 产品发版说明

> **提示：**
>
> 关于社区版与企业版的差异说明及离线文档下载 ，请参见 [常见问题](../QA.md)。

## 2021.02.27 发版说明

2021.02.27 发布了云扩 RPA , 本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2102.8 |
|机器人 |1.1.2102.8|

你可以通过 [云扩控制台](https://console.encoo.com/) 下载并体验相关产品。

#### 【编辑器】

<!--1. 支持流程运行时的[浏览器静默运行](../Activities/AppAutomation/Browser/OpenBrowser.md)，实现机器人后台工作，不干扰前端业务人员，提升用户使用体验。-->
1. 支持从选定组件开始调试流程，方便实施人员快速排查定位异常问题，提升实施人员开发效率。
2. 支持快速搜索当前流程文件中的变量并定位，提升实施人员开发效率。
3. 支持在开始主页中导出项目和删除项目，以便更好地管理与分享项目。

#### 【组件库】

1. 系统 > 文件 > [压缩文件/文件夹](../Activities/System/File/CompresseFile.md)、[解压缩文件](../Activities/System/File/DeCompresseFile.md)，提升实施人员开发效率。
2. 代码工具 > PowerShell > [执行PowerShell代码](../Activities/CodeExecuter/PowerShell/PowerShell.md)，提升实施人员开发效率。
3. 软件自动化 > Office Excel > [替换](../Activities/AppAutomation/OfficeExcel/OfficeExcelReplace.md)，提升实施人员开发效率。
<!--3. 界面自动化 > [设置Web元素属性值](../Activities/UIAutomation/SetWebElementAttributeValue.md)，提升实施人员开发效率。-->

#### 【机器人】

1. 支持在[流程执行页面](../Robot/RunningProcess.md)打开日志文件，提升用户使用体验。

### 改进与增强

#### 【编辑器】

1. 优化版本控制中的版本比对功能的呈现样式为可折叠的树形结构，提升用户使用体验。
2. 优化F4快捷键录制技术后台切换逻辑，可以更智能地自动判断并选择最合适的录制技术，提升用户使用体验。

#### 【组件库】

1. 软件自动化 > Office Excel > [筛选](../Activities/AppAutomation/OfficeExcel/Filter.md)，允许筛选条件中的值为变量类型，扩展了筛选功能的适用范围。
2. 代码工具 > [HTTP请求](../Activities/CodeExecuter/HTTP/HTTPRequest.md)，在原有C#代码模式基础之上，新增支持纯文本输入模式。

## 2021.02.23 发版说明

2021.02.23 发布了云扩 RPA , 本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 控制台|3.0.37424|
| 小程序   | 1.1.1133 |

你可以通过 [云扩控制台](https://console.encoo.com/) 下载并体验相关产品。

### 新增功能

#### 【控制台】

新上线 Console 管理后台，用于对控制台租户、账户等进行管理，提升RPA系统管理员的日常管理工作的效率。主要包括：

1. 新增通过后台查看并管理租户信息。
2. 新增通过后台删除租户。
3. 新增通过后台创建企业版租户及管理员账号。
4. 新增通过后台对控制台用户邮箱后缀进行管理。

#### 【小程序】

1. 新增输入（9个）、展示（2个）、布局（1个）系列组件，开发人员可以更灵活地对小程序页面界面元素进行排版。
2. 新增组件的通用配置、通用样式、事件与行为，开发人员可以更有效地对组件属性及行为进行配置。
3. 新增 [变量管理](../Apps/devApps/appsedit/BasicOperation.md) 功能，使得每个小程序独享一套全局变量，开发人员可以集中管理应用的变量，避免混淆。
4. 支持在小程序开发页面，复制小程序功能，开发人员可以快速克隆并创建新的小程序。
5. 支持在我的小程序页面，复制小程序 URL 功能，方便用户分享“我的小程序”。
6. 在小程序编辑界面中，支持复制已创建的页面和组件等，开发人员可以快速克隆并创建新的页面或组件。
7. 在小程序编辑界面中，支持拖拽改变组件的层级，使组件置于不同的视图下，开发人员可以快速调整组件位置查看显示效果。

### 改进与增强

#### 【小程序】

1. 优化小程序编辑界面、错误页面样式，提升用户体验。

## 2021.01.31 发版说明

2021.01.31 发布了云扩 RPA , 本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2101.8 |
| 机器人 |1.1.2101.8|

你可以通过 [云扩控制台](https://console.encoo.com/) 下载并体验相关产品。

### 新增功能

#### 【编辑器】

1. 企业版支持 [Citrix](../Studio/Extensions/Citrix.md)，使您在 Citrix Desktop 或 Citrix App 上得到和原生自动化方式一样的体验，而无需使用图像识别等自动化技术。
2. 新增 [选择器管理器](../Activities/Appendix/SelectorManager.md) ，用于管理带有“控件元素”或“选择器”属性的组件中的指定元素。
3. 新增 [清理屏幕截图](../Studio/Introduction/TheUserInterface.md)，支持清理项目中未使用到的屏幕截图，减少因截图过多而占用相当大的存储空间。
4. 支持 [搜索](../Studio/quickStart/KeyboardShortcuts.md) 当前流程文件中的组件，以快速定位到该组件。
5. 新增 [快速访问页](../Studio/Introduction/TheUserInterface.md)，可快速打开流程文件、快速进行录制和调试、快速打开实用链接。
6. 新增项目刷新操作，支持刷新当前项目下文件的状态。

#### 【组件库】

1. 软件自动化 > 浏览器 > [关闭浏览器](../Activities/AppAutomation/Browser/BrowserClose.md)，支持关闭所有类型的已打开的浏览器。
2. 代码工具 > 类型转换 > [文本转数值](../Activities/CodeExecuter/TypeConversion/TextToNumbericActivity.md)，实现将文本转换为数值。
3. 代码工具 > 文本 ：[分割文本](../Activities/CodeExecuter/TextProcessing/SplitTextActivity.md)、[追加文本](../Activities/CodeExecuter/TextProcessing/AppendTextActivity.md)。
4. 系统 > [多项选择框](../Activities/System/MultiSelectListBoxActivity.md)：实现以弹框的形式，选择一个或多个选项。
5. 软件自动化 > Office Excel > [取消单元格合并](../Activities/AppAutomation/OfficeExcel/UnMergeCells.md)：实现对指定单元格区域已合并的单元格进行拆分。
6. 代码工具 > 字典：[初始化字典](../Activities/CodeExecuter/Dictionary/InitializeDictionaryActivity.md)、[添加键值对](../Activities/CodeExecuter/Dictionary/AddDictionaryActivity.md)、[获取键值对数量](../Activities/CodeExecuter/Dictionary/GetQuantityOfDictionaryActivity.md)、[是否包含键/值](../Activities/CodeExecuter/Dictionary/ContainsKeyValueActivity.md)、[移除键值对](../Activities/CodeExecuter/Dictionary/RemoveKeyValueActivity.md)、[清空字典](../Activities/CodeExecuter/Dictionary/EmptyDictionaryActivity.md)。
7. 控制台：[上传文件](../Activities/Console/FileUploadActivity.md)、[删除文件/文件夹](../Activities/Console/FileDeleteActivity.md)。

#### 【机器人】

1. 新增 [IBM DB2 扩展](../Robot/Settings/extensions/DB2Extension.md) 来进行 IBM DB2 数据库的自动化。
2. 企业版支持配置 [是否接收控制台调度](../Robot/Settings/Basic.md)，使得机器人未执行控制台调度命令时，仍然可以继续使用该机器人。

### 改进与增强

#### 【编辑器】

1. 优化 UIA3 录制技术，提升稳定性。
2. 优化属性面板界面样式，更改背景色，提升视觉效果。
3. 优化项目面板、组件面板样式，更换图标、间距，提升视觉效果。
4. 优化软件许可协议界面的勾选区域，点击勾选框旁边的文字也可勾选中，提升用户体验。

#### 【组件库】

1. 界面自动化 > [发送快捷键](../Activities/UIAutomation/SendHotkey.md)，新增发送前行为属性，支持点击和设置焦点两种行为。
2. 控制台 > [文档理解](../Activities/Console/DocReader.md)，支持识别图片类型文件。
3. 流程控制 > [重试](../Activities/WorkflowControl/Retry.md)，将条件属性归类至可选项类别中。
4. 系统：优化 [确认框](../Activities/System/ConfirmDialog.md)、[输入框](../Activities/System/InputDialog.md)，支持可以手动复制“描述”信息。
5. 代码工具 > C# > 执行 C#代码，支持输出出错的具体代码位置（行号）及错误信息。
6. 软件自动化 > Office Excel > [排序](../Activities/AppAutomation/OfficeExcel/Sort.md)，支持选择排序方式。
7. 数据库 > [连接数据库](../Activities/Database/ConnectDatabase.md)：优化连接 DB2 数据库界面提示信息。

#### 【机器人】

1. 优化 [正在执行](../Robot/RunningProcess.md) 界面，将标题改为“执行日志”并增加“再次执行”按钮。
2. 优化执行流程时桌面右下角机器人图标，使得机器人图标闪动效果更明显。
3. 优化定时任务，在定时任务开始前 30 秒弹窗提示，避免影响用户手头工作。

## 2021.01.21 发版说明

2021.01.21 发布了云扩 RPA , 本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 控制台   | 3.0.35232 |

你可以通过 [云扩控制台](https://console.encoo.com/) 下载并体验相关产品。

### 新增功能

#### 【控制台】

1. 支持用户删除调度队列。
2. 用户注销后，token 自动过期且不支持访问 API，提升系统安全性。

### 改进与增强

#### 【控制台】

1. 优化控制台核心性能问题。
2. 优化仪表盘时间筛选问及保留精确位数问题。
3. 优化日志详情页面中日志序号及任务列表中序号匹配问题。
4. 优化部分页面在 360、IE 浏览器中的兼容问题。
5. 修复新建对话框会记住上一次新建内容的问题，提升用户体验。
6. 修复系统切换后弹窗异常打开问题。
7. 修复资源组管理添加用户角色时，搜索角色无效的问题。
8. 修复机器人下载文件时的权限问题。
9. 修复资源组删除异常的问题。
10. 修复机器人在多网关实例的环境下无法正常连接的问题。

## 2021.01.07 发版说明

2021.01.07 发布了云扩 RPA , 本次发布的产品及版本号为：
|         | 版本号      |
| -----:  | -----:     |
| 控制台   | 3.0.34008 |

你可以通过 [云扩控制台](https://console.encoo.com/) 下载并体验相关产品。

### 新增功能

#### 【控制台】

1. 控制台首页中新增手机自动化（IOS 和 Android）安装包。
2. 机器人管理页面中新增托管状态，未托管的机器人将不受控制台任务调度。
3. 控制台前端新增超时自动退出系统机制，提升系统安全性。
4. 在调度队列详情中增加任务列表，便于快速管理队列任务。

### 改进与增强

#### 【控制台】

1. 对控制台整体界面样式进行升级，提升用户体验及视觉效果，主要包括：
    - 切换选项卡样式优化
    - 弹窗优化
    - 二级详情页左侧列表优化
    - 二级详情页整体布局及样式优化
    - 部分列表选中状态样式完善

2. 优化英文环境下系统的界面样式。
3. 优化仪表盘数据保留方式。
4. 优化网关调用逻辑，提高并发性能。
5. 优化系统告警提示语。
6. 优化系统邮件发送模板。
