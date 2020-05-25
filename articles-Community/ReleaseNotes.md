# 云扩社区版发版说明

## 2020.05.21 发版说明

2020.05.21 发布了云扩 RPA 编辑器和机器人社区版。
本次发布的编辑器和机器人的版本号分别是：

|         | 版本号      |
| -----:  | -----:     |
| 编辑器   | 1.1.2005.3 |
| 机器人   | 1.1.2005.3 |

你可以通过*云扩 RPA 控制台* -> [*安装包下载*](https://console.encoo.com/#/download) 页面体验相关产品。

### 新增功能
1. 【组件】新增邮件相关的组件“获取邮件(IMAP)”。详情请参看 [获取邮件(IMAP)](Activities/AppAutomation/Mail/GetMailIMAP.md?_v=Community)。
2. 【组件】新增Office Excel相关的组件“自动填充”。详情请参看 [自动填充](Activities/AppAutomation/OfficeExcel/AutoFillRange.md)。
3. 【组件】新增剪贴板相关的组件“设置剪贴板文本”。详情请参看 [设置剪贴板文本](Activities/System/SetContentsToClipboard.md) 。
4. 【组件市场】新增对 Office PowerPoint 支持的组件包。详情请查看[OfficePPT组件包](https://marketplace.encoo.com/#/activity/detail?packageId=Encootech.OfficePPT)。
5. 【组件市场】新增语音识别组件包。详情请查看[竹间智能语音识别](https://marketplace.encoo.com/#/activity/detail?packageId=Emotibot) 。
6. 【组件市场】新增发票识别组件包，详情请查看[国票信息发票组件包](https://marketplace.encoo.com/#/activity/detail?packageId=NationalEBill)。
7. 【编辑器】支持将流程中的组件保存为子流程文件。你可以使用本功能将复杂流程拆解为多个简单的流程。
8. 【编辑器】支持通过组件的右键菜单，访问组件的帮助文档。
9. 【编辑器】在创建变量/参数时，支持快速创建 DataTable / IUiObject 类型的变量/参数。

### 增强功能
1. 【组件】提升 Office Excel 组件执行性能。
1. 【机器人】增强机器人执行稳定性。
1. 【编辑器】增强了表达式编辑器的智能感知功能，支持变量/参数/方法名称联想。
1. 【编辑器】针对社区版许可证超出配额的情况，增加解决方法的提示。

### 修复问题

1. 【编辑器】修复了表达式编辑时，自动补入变量名不齐全的问题。
1. 【编辑器】修复了调试时不能查看容器类组件中最后一个组件的属性的问题。
1. 【编辑器】修复了搜索组件时，搜索结果展示不全的问题。
1. 【编辑器】修复了修改变量值后，调试项目时，修改不生效的问题。
1. 【编辑器】修复了编辑器界面偶尔无法点击的问题。