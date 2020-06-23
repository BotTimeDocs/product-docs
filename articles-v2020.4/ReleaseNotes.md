# 云扩产品发版说明

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
2. 【编辑器】新建项目时支持选择桌面录制技术-UIA/UIA3。
3. 【编辑器】支持删除命名空间。
4. 【编辑器】支持设置运行时是否最小化编辑器主界面。
5. 【编辑器】支持更多的快捷键。详情请参看[键盘快捷键](./Studio/Introduction/KeyboardShortcuts.md)。
6. 【组件】新增“设置日期和时间”组件。详情请查看[设置日期和时间](Activities/System/SetDateTime.md)
7. 【组件】新增“选择文件”及“选择文件夹”对话框组件。详情请查看[选择文件](Activities/System/File/SelectFile.md?_v=v2020.4)与[选择文件夹](Activities/System/File/SelectFolder.md)
8. 【组件】新增Office Excel"设置文字颜色"组件并使用拾色器提升颜色设置体验。详情请查看[设置文字颜色](Activities/AppAutomation/OfficeExxcel/SetTextColor.md)
9. 【机器人】执行本地流程时支持填写流程参数


### 增强功能

1. 【编辑器】输出面板改造等界面优化。
2. 【编辑器】项目打开及编译错误详细化，更易定位错误位置。
3. 【编辑器】在编辑区域，支持通过组件的右键菜单，访问组件的帮助文档。
4. 【组件】优化Office Excel“排序”组件：支持指定开始行号。详情请查看[排序](Activities/AppAutomation/OfficeExxcel/Sort.md)
5. 【组件】优化Office Excel“设置单元格背景色”组件：使用拾色器提升颜色设置体验。详情请查看[设置单元格背景色](Activities/AppAutomation/OfficeExxcel/SetCellBackcolor.md)


### 修复问题

1. 

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
2. 【组件】新增Office Excel相关的组件“自动填充”。详情请参看 [自动填充](Activities/AppAutomation/OfficeExcel/AutoFillRange.md?_v=v2020.4)。
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