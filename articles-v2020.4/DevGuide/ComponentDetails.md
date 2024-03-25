# 指南二 《组件详解》

<br>

>导读: 
> 
>重在带大家了解云扩编辑器流程编辑中，会使用到的组件概念、不同组件类型及使用用途。

<br><br>

## 一、组件概念简介

<br>

### 1.1 什么是组件？

组件是模拟人们在计算机上操作软件的某个行为或动作，把实际工作中的业务场景以[自动化](../AutomationPrinciples.md)的方式实现。

例如：登录某页面时，需要输入【用户名】和【密码】并点击【登录】按钮，这其中包含三个操作，分别为：
1. 在用户名输入框中输入账号信息；
2. 在密码输入框中输入密码；
3. 鼠标点击登录按钮。

这三个动作在页面上可以分别使用三个组件来完成。

那么多个组件串联后便形成了**流程**。例如在成功登录软件后，继续点击某个页面控件，那么在流程设计工具中再加入操作这个控件的组件就可以完成后续操作了。


<br><br>

### 1.2 组件的组成部分

单个组件是由组件名称、组件面板、弹窗和属性栏构成。用于表达使用什么组件在什么位置和条件下做什么操作。

<br>

- **组件名称**：通常可以理解为是某个“操作”行为的步骤名称。在开发过程中也可以自定义，达到更符合业务逻辑和更容易被理解的名字



- **组件面板**：在开发工具的流程设计面板中展示当前组件的属性，以便于在属性中填写数据


- **弹窗**：以弹窗的方式展示当前组件的属性，以便于在属性中填写数据


- **属性栏**：在开发工具中以独立模块展示组件所有属性，以便于在属性中填写数据

<br>
如下图示：

在流程设计面板中添加了一个名称[写入单元格](../Activities/AppAutomation/OfficeExcel/WriteCell.md)的组件，并在此组件的属性“工作表”、“单元格”、“数据”中分别填写了数据“Sheet1”、“A1”和“Hello RPA”，

用于实现在excel文件中的工作表“Sheet1”和单元格“A1”位置，写入了一段文本“Hello RPA”

<img width='600' src="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/componentsexample.png"/>
 
> **注意**：
> 
> - 属性由组件本身定义，一个组件包含一个或多个属性
> - 数据由开发者在对应的组件属性中输入，数据可以是一段字符串、[变量](../Studio/process/developProject/Variables/Variables.md)或[参数](https://Studio/process/developProject/Arguments/Arguments.md)
> - 字符串类型的数据需包含在英文双引号””中
> - 示例中的[写入单元格](../Activities/AppAutomation/OfficeExcel/WriteCell.md)组件需要包含在容器类组件类别的[打开/新建Excel](https://Activities/AppAutomation/OfficeExcel/OpenExcel.md)组件中使用
> - 对网页中需要自动化的场景需指定页面元素定位并实现自动化，参考[元素详解](../AutomationPrinciples.md)

<br>

### 1.3 组件类型

在[云扩RPA编辑器](https://academy.encoo.com/zh-cn/wiki/Studio/README.md)的[内置组件库](https://academy.encoo.com/zh-cn/wiki/Activities/PageAction/Click.md)中包含300+组件，可直接拖拽到设计面板使用，也可以直接从云扩[组件市场](https://marketplace.encoo.com/#/activity?lang=zh-cn)中下载。另外也支持开发者自研发的组件发布到团队市场。

- 内置组件：由云扩开发团队提供并内置在编辑器[组件库](https://academy.encoo.com/zh-cn/wiki/Activities/PageAction/Click.md)中，直接拖拽至流程设计面板即可使用。
- 市场组件：由开发者提供的公开组件库，从[组件市场下载](../Studio/market/activityMarket.md)后即可使用。
- 团队市场组件：**云扩为开发者默认提供团队市场空间，无需开发者再自己配置，可直接将开发好的组件上传到团队市场，实现团队内部共享**。

另外，如果需要自定义配置市场，详见[自定义配置](https://academy.encoo.com/zh-cn/wiki/BestPractices/offline-use-activitymarket.md)。

<br>

### 1.4 如何找到组件？

可以通过关键字(中文、英文、拼音、别名)在编辑器[组件库](https://academy.encoo.com/zh-cn/wiki/Activities/PageAction/Click.md)或[组件市场](https://marketplace.encoo.com/#/activity?lang=zh-cn)中查找。

<br><br>

## 二、组件类别：功能类/容器类

组件主要分为功能类组件和容器类组件

<br>

### 2.1 功能组件主要分为以下几种类别：
<br>

**（1）页面动作**： 实现对网页/桌面软件界面上的各种元素控件一系列的自动化操作，例如：使用[输入文本](../Activities/UIAutomation/TypeInto.md)组件在百度搜索框内输入关键字“RPA”，再使用[点击](../Activities/UIAutomation/Click.md)组件点击搜索按钮开始对”RPA”搜索，使用[获取结构化数据](../Activities/UIAutomation/ExtractStructuredData.md)组件把搜索结果列表或表格数据抓取。其他在页面上的操作像获取界面文字、截图等都可以在此目录下找到相应的组件；


**（2）鼠标/键盘**：

模拟我们在计算机上的鼠标或键盘上的常用操作，例如：使用[发送快捷键](../academy.encoo.com/wiki/Activities/UIAutomation/SendHotkey.md)组件实现快捷键操作；使用[移动鼠标](../Activities/UIAutomation/MoveMouse.md)组件将鼠标焦点移动到屏幕某个位置；使用[滚动鼠标](https://academy.encoo.com/wiki/Activities/MouseKeyboard/rotate-wheel.md)组件滑动页面上的滚动条，查看页面下方的内容。


**（3）浏览器**：实现对浏览器的基本操作，例如：在百度页面输入关键字查询，需要先使用[打开浏览器](../Activities/AppAutomation/Browser/OpenBrowser.md)组件把百度页面打开，再把[输入文本](../Activities/UIAutomation/TypeInto.md)组件拖入到其内部，对搜索框定位和填写关键字。


**（4）表格/Excel/WPS**：实现对常用办公软件 Office Excel 和 WPS自动化操作，例如：使用[打开/新建](../Activities/AppAutomation/OfficeExcel/OpenExcel.md)组件自动创建新文件或打开已有文件，使用[写入区域](../Activities/AppAutomation/OfficeExcel/WriteRange.md)或[写入单元格](../Activities/AppAutomation/OfficeExcel/WriteCell.md)等组件向Excel文件填写数据，还可以使用[插入公式](../Activities/AppAutomation/OfficeExcel/InsertFormula.md)组件对数据处理等。其他对Excel/WPS的一些常用操作都可以在此目录找到相应组件；


**（5）邮件**：实现对常用邮箱服务Outlook、Exchange以及IMAP、POP3、SMTP协议的操作，例如：使用[发送邮件(Outlook)](../Activities/AppAutomation/Mail/SendOutlookMail.md)或[发送邮件(SMTP)](../Activities/AppAutomation/Mail/SendMailSMTP.md)组件对指定人发送邮件，使用[获取邮件(Outlook)](../Activities/AppAutomation/Mail/GetOutlookMail.md)或[获取邮件(POP3)](../Activities/AppAutomation/Mail/GetMailPOP3.md)获取收件人邮箱中的邮件；


**（6）PDF**：实现对PDF文件的提取文档内容、合并文档等基础操作，例如：使用[合并文件](../Activities/AppAutomation/PDF/MergePDF.md)组件把多个PDF文件合并为一个文件；使用[读取文本](../Activities/AppAutomation/PDF/ExtractText.md)组件把PDF文件中的内容提取出来；


**（7）文件/文件夹**：实现对计算机上的文件夹或文件的常用操作，例如：使用[遍历文件夹](../Activities/System/File/ForeachFolder.md)组件循环拿到指定文件夹下的所有类型或特定类型的文件路径，再使用[复制/移动文件](../Activities/System/File/CopyOrMoveFile.md)组件把需要挪动位置的文件移动到其他文件夹；


**（8）判断/循环**：用于对特定数据做判断或循环处理，例如：使用[循环操作(For Each)](../Activities/WorkflowControl/Loop/ForEach.md)循环数组变量数据，使用[条件(if)](../Activities/WorkflowControl/Determine/If.md)组件判断变量 FileName = ABC 时，把变量 FileName 更改值为 ABCD；


**（10）应用程序**：用于操作计算机软件程序或进程，例如：使用[打开程序](../Activities/System/Application/OpenApplication.md)组件打开记事本程序或使用[关闭进程](../Activities/System/Application/CloseProcess.md)关闭记事本程序的进程；


**（11）操作系统**：用于对计算机操作系统上的基础操作，例如：使用[解锁](../Activities/System/Screen/WindowsUnlockActivity.md)组件对屏幕解锁，使用[输入框](../Activities/System/InputDialog.md)组件在流程运行时弹窗接收用户在弹窗中输入的数据，也可使用[执行命令行](../Activities/System/ExecuteCMD.md)组件在cmd中执行命令。


**（12）AI**：此目录下包含云扩自研和常用AI平台（阿里云、百度AI等）及服务（[身份证识别](../Activities/AI/IdCardIdentification.md)、[发票识别](../Activities/AI/VATInvoiceIdentification.md)等）封装的组件，可以直接拖拽至流程中使用，无需再写代码开发。例如：使用增值税发票识别组件或身份证识别对图片文件进行OCR识别, 参考示例课程[批量提取发票数据](../ExampleCourse/OCRInvoice.md)。


**（13）开发服务**：建立了开发者与[云扩超自动化平台](https://academy.encoo.com/zh-cn/wiki/Reference/Console/README.md)在线服务的关联，可以在流程中直接操作云扩超自动化平台中的[资产](../Console/datacentor/asset/AboutAsset.md)、[文件](../Console/datacentor/fileservice/Aboutfileservice.md)等服务。例如：使用[设置资产](../Activities/Console/set-assets.md)组件对指定的资产设置数据，使用[下载文件](../Activities/Console/FileDownloadActivity.md)组件从文件服务中下载指定的文件到本地；

**（14）代码编程**：为开发者提供了在流程开发过程中编写C#、Python等代码的功能，例如：可以使用[执行C#代码](../Activities/CodeExecuter/CSharp/ExecuteCSharp.md)或[执行Python代码](../Activities/CodeExecuter/Python/PythonExcuteFile.md)组件编写C#或Python代码；


**（15）数据处理**：用于对流程中的变量做处理，例如：使用[赋值](../Activities/WorkflowControl/Assign.md)组件对变量赋值，使用[数据表](../Activities/DataTable/BuildDataTable.md)系列组件对DataTable类型变量操作，使用[数据格式化](../Activities/CodeExecuter/DataProcessing/FormatData.md)组件对字符串转换成货币、日期和时间、百分比等格式。同样对JSON、数组等变量的操作和使用正则表达式处理文本等也可在此目录找到相应组件；


**（16）触发器**：用于在流程中监听键盘、鼠标、邮箱、文件中的事件变化，例如：可以使用[鼠标触发器](../Activities/Triggers/SystemTrigger/mousetrigger.md)监听鼠标的单击、双击等事件；使用[邮件触发器(Outlook)](../Activities/Triggers/OutlookTrigger.md)监听Outlook是否有新邮件等事件；


**（17）数据库操作**：用于对Oracle、MS SQL、MySQL等常用数据库的操作，例如：先使用[连接数据库](../Activities/Database/ConnectDatabase.md)组件连接到目标数据库，使用[执行语句](../Activities/Database/ExecuteNonQuery.md)组件执行数据库脚本；


**（18）流程控制**：用于控制整个流程的运行逻辑，例如：在流程中使用[流程判断](../Activities/WorkflowControl/Flowchart/Decision.md)组件决定执行逻辑A或逻辑B，使用[调用子流程](../Activities/WorkflowControl/InvokeWorkflow.md)组件在流程某个节点调用子流程文件；


**（19）SAP**：此目录下是为SAP软件定制化的组件，实现对SAP的常用操作。例如：使用[登录应用](../Activities/UIAutomation/SAP/SAP_Login.md)组件登录SAP，使用[执行事务](../Activities/UIAutomation/SAP/SAP_Transaction.md)组件在SAP中执行事务代码；


**（22）高级自动化**：此目录为中高级开发者提供了高级自动化的操作，例如：使用[绑定远程桌面](../Activities/UIAutomation/Window/SetWindowState.md)组件实现远程桌面操作，使用[获取屏幕文本](https://academy.encoo.com/wiki/Activities/PageAction/Screenshot.md)组件获取特殊界面难以读取的文本数据；


**（23）手机自动化**：用于实现在手机端的自动化操作，支持iphone与android，例如：先使用[连接设备](../Activities/PhoneAutomation/MobileConnect.md)组件连接到手机，使用此目录下的[点击](../Activities/PhoneAutomation/MobileTap.md)组件完成在手机界面的点击操作。

<br><br>

### 2.2 容器类组件

> **容器类组件**指确定一个操作范围，并在其内部使用特定自动化组件完成操作。
> 
> 例如在实际工作中操作excel文件，我们需要先打开excel文件才能完成填写数据、设置公式、制作透视表等操作，
那么当前操作的Excel文件就是“容器”，写入数据、设置公式等操作是必须在Excel文件内才能完成的操作。同理，在RPA自动化过程中也是同样的逻辑完成自动化操作。

常用容器类组件:

- [打开/新建Excel](../Activities/AppAutomation/OfficeExcel/OpenExcel.md)：用于打开一个 Excel文件并为 Excel系列组件操作提供范围，以完成对当前Excel文件的自动化操作。
- [打开浏览器](../Activities/AppAutomation/Browser/OpenBrowser.md)：用于打开一个特定类型的浏览器（Chrome/Edge/Firefox等）确定后续操作范围，以完成在当前浏览器上的页面自动化操作。
- [连接数据库](../Activities/Database/ConnectDatabase.md)：用于连接到指定的数据库并为数据库系列组件提供操作范围，以完成对当前数据库的自动化操作。
- [打开应用程序](../Activities/System/Application/OpenApplication.md)：用于打开一个桌面软件应用确定后续操作范围，以完成对当前桌面应用的自动化操作。
- [Python环境](../Activities/CodeExecuter/Python/PythonScope.md)：用于确定计算机上安装的Python环境，以执行Python代码组件。
- [连接设备（手机）](../Activities/PhoneAutomation/MobileConnect.md)：用于连接到指定的手机，以确定流程在哪台设备上运行，同时为放在该组件内的手机自动化组件提供运行的范围，实现手机自动化。

## 三、如何自研组件？

为了满足多种多样的业务需求，更有效率的实现自动化操作，云扩开放了两种方式让开发者可以根据实际需要自定义组件。

你可以通过以下两种方式实现：

- [在编辑器中使用组件项目自定义](../Studio/process/CreateProject/CreateLibrary.md): 可以使用无代码的方式在编辑器中创建组件项目自定义组件。
- [在Visual Studio中编程实现](../c9vrjkv7og.feishu.cn/file/boxcnnIGLuSOHvKycnUueDmnqHh): 如果你是一名.NET开发者，可以选择使用此方式在Visual Studio中编码开发组件。

