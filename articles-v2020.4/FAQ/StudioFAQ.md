# 编辑器 FAQ

## 安装相关

1. **Q：安装时弹出程序崩溃提示，如何解决？**

   ![安装崩溃](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/installCollapse.png)

   **A：** 打开“控制面板 > 程序 > 卸载程序”，在卸载或更改程序列表中检查是否安装“.Net Framework 4.6.1 ”及以上版本的“.Net Framework 环境”。
   如果未安装，请先下载“[.Net Framework 4.6.1](https://www.microsoft.com/zh-CN/download/details.aspx?id=49982)”并安装，安装好之后重启电脑再进行云扩 RPA 编辑器的安装。

2. **Q：点击安装，显示安装失败**

   ![安装失败](https://docimages.blob.core.chinacloudapi.cn/images/Studio/installfailed20210824.png)

    **A：**

    - 排查步骤 1：检查杀毒软件是否正在运行，关闭杀毒软件(如，360 软件)后重新安装。

    - 排查步骤 2：检查当前用户在安装目录的读写权限，如果当前用户在安装路径没有读写权限，则要用管理员账号登录，在安装目录右键，点击属性，点击安全标签，添加目标账户，并添加完全控制权限，最后点击确定，然后退出管理员账号，用目标用户登录进行安装。

3. **Q：编辑器的默认安装目录是什么？**

    **A：** `%UserProfile%\AppData\Local\Encoo Studio`

4. **Q：已安装机器人后安装编辑器，报错“错误消息：未将对象引用设置到对象的实例”。**

    ![安装报错](https://docimages.blob.core.chinacloudapi.cn/images/Studio/studioinstallerror20210825.png)

    **A：** 可检查是否安装“.net 中文语言包”，如果安装了，可以卸载后再尝试，如果没有安装，可检查日志。

    ![中文语言包](https://docimages.blob.core.chinacloudapi.cn/images/Studio/dnetpackage20210825.jpg)

5. **Q：Windows XP 系统的计算机，可以安装 RPA 的客户端吗？**

    **A：** 不支持，RPA 大部分产品都是新型产品，诞生的时间比 XP 系统要晚很多，所以版本适配一般都是 Win7 版本及以上。

## 激活/许可证相关

1. **Q：编辑器许可证已过期，是否需要应用新的许可证？企业版的没联网是否就会出现此弹窗提示？**

    **A：** 没有网络无法使用社区版编辑器。联网激活企业版编辑器，使用也需要联网，许可证激活可以断网使用。

2. **Q：编辑器登录时无法激活，提示“没有可用的许可证”，是什么原因？换了电脑后如何解绑？**

    **A：** 社区版只有一个 RPA 编辑器可以使用， 确认是否已激活一个编辑器了？可登录控制台，点击“许可证” 菜单，进行解绑。

    ![许可证](https://docimages.blob.core.chinacloudapi.cn/images/Studio/license20210825.png)

## 卸载相关

1. **Q：卸载失败**

   **A：**

   (1) 安装目录(Program files x86)，25 版本以后的安装目录在用户目录 `AppData\Local\`，下面 encootech 文件夹删掉

   (2) `C:\ProgramData\Package Cache\` 里面搜一下 Digi4th 开头的，都删掉

   (3) 删除 windows 服务 DataBusService(cmd 命令行 `sc delete DataBusService`)

## 系统日志相关

1. **Q：编辑器的系统日志的默认路径是什么？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Log`。

2. **Q：编辑器的安装日志的默认路径是什么？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Installation`。

## 项目/流程相关

1. **Q：使用标准流程模板创建的流程，日志目录配置好了，但其实没有创建日志文件在配置的目录下。**

    ![日志路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/logpath20210826.png)

    **A：** 日志文件路径这里是把上面两个变量连在一起的，只要设置日志文件夹路径和日志文件名即可。如果没设，默认应该是在桌面上有个日志文件夹，里面有日志文件。

2. **Q: 建了两个项目，如何才能把两个项目合并，使得打开编辑器时两个都可以看到？**

    **A：** 可在需要保留的项目中把另外一个项目的 xaml 文件都导入过去。

    ![导入文件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Importproject20210824.png)

3. **Q：新建了一个项目，报错：[错误] 未能从程序集“BotTimeUI.Common, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null”中加载类型“BotTimeUI.Common.Utility.ChildrenAccessWay”。**

    **A：** 如果是新安装的编辑器，可能是和其他版本冲突了。先关闭编辑器，在 `C:\users\<user>\.nuget` 下面，将 packages 文件夹重命名，相当于备份，然后重新打开编辑器，新建项目。

4. **Q：如何处理管理员运行的市场组件，仍提示该组件需要使用管理员方式运行编辑器？**

    **A：** 编辑器以管理员身份运行，在项目空白处右击，选择“项目设置 > 常规”，勾选以管理员方式运行。

    ![项目设置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/projectsetting20210826.png)

5. **Q：怎样用管理员权限执行“执行命令行”组件?**

    ![执行 cmd 命令](https://docimages.blob.core.chinacloudapi.cn/images/Studio/cmd20210826.png)

    **A：** 在“项目设置”里勾选“以管理员权限运行”。

6. **Q：执行流程时，报错“需要提升权限才能识别此应用。请尝试以管理员身份启动录制程序。”**

    **A：** 可以右键点击项目“项目设置 > 常规”，勾选以管理员方式运行。

7. **Q：有什么办法快速转换到流程项目吗？**

    **A：** project.json 文件里面，把 `ProjectType` 的值改成 `Workflow`，project.runtime.json 里面也改下。

8. **Q：编辑器流程中的组件未显示，报错“未能生成 BrowserOpen 的视图”。**

    **A：** 按照如下步骤进行处理：

    - step1: 关闭编辑器
    - step2：在文件资源管理器输入目录：`%userprofile%\.nuget\packages\automationactivity`，然后重命名此文件夹，如 `automationactivity01`
    - step3：重启编辑器

9. **Q：提取为子流程是否有前提条件？“提取为子流程”菜单为啥是灰色不可用？**

    **A：** 提取子流程只能选单个组件（序列、流程图也可以），可以把这些组件放到一个流程图里，然后把这个流程图提取为子流程。

10. **Q：怎样能把在一台电脑做好的流程，导出来作为另一台电脑做的流程的子流程？**

    **A：** 导出流程，拷贝到另一台电脑并导入进依赖项，然后使用“调用流程（引用项目）”组件调用该流程。

11. **Q：流程图、序列、状态机三者有什么区别？**

    **A：**
    - **流程图** 适用于复杂的业务场景，通过流程控制类组件（如流程决策）可以创建复杂的流程；
    - **序列** 是一种线性的工作流，内部流程按顺序执行，可以充当单个组件块重复使用；
    - **状态机** 是以事件驱动方式模块化工作流程，根据不同的事件发生相应的动作进行状态改变。

## 调试/运行相关

1. **Q：如何执行项目下其他的 xaml 文件，按 F5 编辑器默认从 Main.xaml 执行。**

    **A：** 右键点击有执行快捷键：`F6` 可调试当前打开的流程，`Ctrl+F6` 可运行当前打开的流程。

2. **Q：通过设置断点调试流程，是否指运行到断点就停止了？如果需要恢复应该如何操作？**

    **A：** 断点只是调试用的，不影响运行，停下后在左侧面板点击“继续”还会继续往下跑的。如果需要恢复，右击“删除断点”即可。

3. **Q：执行流程时报错“[错误] 未将对象引用设置到对象的实例。”**

    **A：** 一般情况下是流程中用到的某个变量没有值。

## 市场相关

1. **Q: 从组件市场安装的组件包存放在本地计算机什么路径下？**

    **A：** `%UserProfile%\.nuget\packages`

2. **Q：如何将组件市场中的 FlexGrid 组件安装至离线的编辑器环境中？**

    **A：** 导出项目的时候勾选包含依赖项，或者在离线环境建一个私有市场，私有市场也需要把有网环境的.nupkg 文件复制过去，`%userprofile%\.nuget\packages`

    ![组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/activitymarket20210825.png)

3. **Q：编辑器调用 C#代码的时候如何引用第三方类库？需要做一个企业内网的 IMAP 协议接受邮件的脚本，编辑器的 IMAP 接受邮件组件一直报错。**

    ![报错信息](https://docimages.blob.core.chinacloudapi.cn/images/Studio/imap20210825.png)

    **A：** 在“代码市场”中引用“.net”, 另外“安全连接”选否。

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/codemarket20210825.png)

4. **Q：鼠标拖动滑块只能匀速吗？**

    **A：** 云扩市场组件提供了两个模拟滑动组件，一个是支持加速度拖动，一个是支持根据事先录制的轨迹来滑动。

    ![市场组件滑块](https://docimages.blob.core.chinacloudapi.cn/images/Studio/slider20210902.png)

5. **Q：在代码市场中安装的 C#包，如何引用？**

    **A：** 手动导入命名空间即可在 c# 组件中测试。

6. **Q：如何在内网创建项目并使用组件市场的组件？**

    **A：** 从组件市场下载的组件包在目录下(%userprofile%\.nuget\packages)，可以从此拷到内网的电脑中，例如，放在 "c:\activities"，再把 "c:\activities" 设置为本地组件市场即可。

7. **Q：如何在 C#代码编辑器中引用.dll 文件？**

    **A：** 主要是通过代码市场，具体可参见 [如何在 C#代码编辑器中引用.dll 文件](https://community.encoo.com/thread/510)。

## 插件/扩展相关

1. **Q: 怎么安装 chrome 扩展？**

    **A：** 打开编辑器，在 **开始 > 工具 > 扩展** 中，选择并点击“Chrome 扩展”，根据提示操作即可。（在安装后，请手动打开浏览器并输入：chrome://extensions/，启用扩展。）

    ![安装扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/extensioninpath20201019.png)

2. **Q: Chrome 录制失败，无法与 Chrome 扩展通信？**

    **A：** 若出现无法与浏览器扩展通讯的提示，可按照如下步骤排查：

    (1) 检查 chrome 浏览器扩展，是否安装了 chrome 扩展并且启用，如果未安装“云扩录制器”扩展，需要 [通过 Studio 进行自动安装](./../Studio/Extensions/ChromeExtension.md)。

    ![启用扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/chrome-usingExtension.png)

    (2) 当打开 chrome 后，检查“任务管理器”中是否存在 EncooNativeMessageHost.exe 进程：，该进程是 RPA 与 chrome 浏览器的通信进程，如果不存在，则检查(1)。

    > **说明：**
    >
    > - **如果 EncooNativeMessageHost.exe 进程未启动**，需暂时关闭杀毒软件的防护功能，然后 [通过 Studio 进行自动安装](./../Studio/Extensions/ChromeExtension.md)。
    > - **如果 EncooNativeMessageHost.exe 进程未启动且已经关闭杀毒软件并安装了扩展**，需暂时关闭杀毒软件的防护功能并删除“C:\Users\当前用户\AppData\Local\Encoo\messagehost”文件夹，然后再次通过 Studio 进行安装扩展。
    > - **如果杀毒软件暂时无法关闭，需要公司超级管理员授权才可关闭时**，请用可修改注册表的用户登录，手动修改注册表，[手动安装 Chrome 扩展](./../Studio/Extensions/ChromeExtension.md)。

    ![检查进程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/taskManager.png)

3. **Q: 项目换了电脑后，为什么浏览器打开会闪退？**

    **A：** Chrome 浏览器安装扩展后并启用。

## 发布相关

1. **Q：写好的 xaml 如何部署至机器人，部署至机器人后是否能每天做定时任务？**

    **A：** 编辑器中的流程，通过如下方式部署至机器人:

    - 方式一：在编辑器中将流程导出为 dgs，然后在机器人的“流程库 > 本地流程库”中导入已导出的 dgs 流程包。
    - 方式二：使用编辑器将流程 [发布至机器人](../Studio/process/PublishProject.md)

    部署至机器人后可以设置 [定时任务](../Robot/CronJob.md)。

2. **Q: 文件包的形式如何导入到控制台？是否只能导入 dgs 格式的项目？**

    **A：**
    - 方式一：在编辑器中将流程导出为 dgs，然后在控制台的“流程包管理”中上传已导出的 dgs 流程包。
    - 方式二：从编辑器中将流程 [发布至控制台](../Studio/process/PublishProject.md)。

3. **Q：开发完成了的流程在哪里部署？**

    **A：** 开发完成了的流程，可以点击编辑器菜单栏中的“发布”菜单，可将流程发布至控制台、机器人、流程市场等。

## 元素捕捉相关

1. **Q: 使用组件中的“指定元素”指定浏览器时，无法定位到目标应用程序，验证失败。**

    ![指定元素验证失败](https://docimages.blob.core.chinacloudapi.cn/images/Studio/locateelement20210603.png)

    **A：** 观察目标 title 的特征，如果目标 title 为动态的，把动态字段的值用*来代替。

2. **Q：为什么结构化数据经常获取失败，报错“[错误] 获取结构化数据失败。详细错误信息：操作已超时。”**

    **A：** 是定位失败，编辑时的定位选择和运行时不一样了，要检查哪个属性发生了变化。

3. **Q：有个流程每天运行，不定期会偶发某个组件元素定位失败，但调查问题组件无法再现问题，整体流程稳定性很差，是否有改进方法？（流程操作：桌面 CMS 程序，win10 系统）**

    **A：** 这与系统元素的响应时长有关，建议在出问题的组件上加延迟，或在此步骤前使用等待元素出现组件。
    一般有以下几种方式增加稳定性，增加超时时间、重试、机器人运行出错时截图，在使用前先等待元素出现。exe 应用程序出错时，建议排错期间先不要关闭，查看此时能否验证成功。

4. **Q：如何精确定位到 Excel 内的 button？**

    **A：** 录制技术切换至 IA。

5. **Q：无法识别到指定的元素，怎么处理？**

    ![无法识别按钮](https://docimages.blob.core.chinacloudapi.cn/images/Studio/f420210826.jpg)

    **A：** 用“坐标点击”组件试试，或者 F4 切换一下识别方式。

6. **Q：定位元素超时，无法正确定位？**

    **A：** 可以尝试

    - 切换识别方式，录制时按 F4
    - 用图像识别，录制时按 Ctrl

7. **Q：使用点击组件无法选中 QQ 输入框，无法捕捉元素，怎么办？**

    ![QQ 输入框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/QQInputbox20210902.png)

    **A：** 这个登录界面有个蒙板，确实不好定位。可以选中那个大框后，点开元素探测器，在里面可以选到用户和密码框。

8. **Q：在浏览器上点击链接打开新的浏览器窗口，运行的时候新窗口上的内容一直不能正常执行，总是报错: 操作已超时。**

    **A：** 可能是新窗口上的元素没定位成功，需检查定位的元素里有哪些可能是动态变化的。在选择器编辑器中把可能发生变化的部分用 `*` 代替。

    ![选择器编辑器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/selector20210825.png)

9. **Q：选择器中是否可以写变量？**

    **A：** 可以的，`{{变量名}}`。

10. **Q：在选择器里面可以写 row [0].tostring()这种类型的吗？**

    **A：** 不可以，变量替换必须是基础变量。

11. **Q：弹出窗口的文本框数据无法自动输入，报错“[错误] 输入文本失败。详细错误信息：操作已超时。”**

    **A：** 勾选生成 XPath（仅支持 WEB），然后重新指向元素，`//label[@for='confCode']/..//input[contains(@placeholder,'变量代码')]`

    ![xpath](https://docimages.blob.core.chinacloudapi.cn/images/Studio/xpath20210826.png)

12. **Q：如何取消掉网页端 Input 标签的 Readonly 属性？**

    ![readonly](https://docimages.blob.core.chinacloudapi.cn/images/Studio/readonly20210826.png)

    **A：** 设置元素属性 `Readonly =""`。

13. **Q：使用 Chrome 浏览器打开 SAP 浏览器页面，页面上的内容无法获取，但是录制时，在选择器中验证是通过的，这个要怎么处理？**

    ![SAP 页面](https://docimages.blob.core.chinacloudapi.cn/images/Studio/sap20210826.png)

    **A：** 用 Xpath，`//input[@title='公司代码']`，改成 `*` 就可以了。

    ![SAP_Xpath](https://docimages.blob.core.chinacloudapi.cn/images/Studio/SAPtitle20210826.png)

14. **Q：有个动态网页，怎么让它不是每次都能输入文本？已经试了通配符 `*` 或 `?` 都识别不到，这有什么好方法？**

    **A：** 只有 `id` 在变，用其他 `sinfo` 或者 `CssSelector` 属性试试，属性值用元素探测器获取到填进去，截取到 iframe 的位置。

    ![CssSelector](https://docimages.blob.core.chinacloudapi.cn/images/Studio/cssselector20210826.png)

15. **Q：在桌面软件界面上定位不到元素，需要如何解决？**

    **A：** 外层定位到弹窗以后，使用图像识别功能进行录制。使用“点击”组件录制的时候定位到弹出窗时，按下 ctrl 键盘，框选一下那个关闭按钮就可以了。

16. **Q：如何实现点击菜单中的子菜单？**

    ![点击子菜单](https://docimages.blob.core.chinacloudapi.cn/images/Studio/clicksubmenu20210826.png)

    **A：** 使用“点击”组件继续点击黄色框的部分，录制时候按 F2，延迟后录制，另外设置一下点击前后的延迟时间。

17. **Q：无法获取页面上显示的数字，F12 查看是乱码，使用获取结构化数据组件查看也是乱码，如何解决？**

    ![F12 页面显示](https://docimages.blob.core.chinacloudapi.cn/images/Studio/F12view20211018.png)

    **A：** 使用 **截屏** 组件截图后，再使用 **OCR 图像识别** 组件识别。

## 数据类型/语法相关

1. **Q：String 类型如何转化为 int？**

    **A：** Convert.ToInt32("String 字串")。

2. **Q：如何用变量计算时间差？比如从网页上获取了一个文本，转换为时间格式后，如何计算时间和自己当前操作时间的时间差？**

    **A：** 可参见 [C#日期加减](https://www.cnblogs.com/RCJL/p/12930425.html?wework_cfm_code=OTcx9KzwohAgedF7GMK4w2wgfzzAnXYvJkWj%2BfQlKu2ufHEl5IWDPUfA5BGsjcdX02a8d5HRYX8WgPkozEyQ1Q7DOODUJ1%2F2Iej2z%2FE1Bpbs4YNG7XGzAoI%3D)。

3. **Q：字符串中如果包含双引号，是否可以使用转义字符？**

    **A：** 可以，两个双引号代表一个双引号。

4. **Q：这个同样的语句，为什么在另一个组件里面调试正常，到这里就报错？**

    ![类型转换错误](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeconverterror20210824.png)

    **A：** Substring(7,4) ，不是 SubString(7,4)，存在拼写错误。

5. **Q：赋值文件名给变量，怎么写，item 有属性表示文件名的吗？**

    **A：** `System.IO.Path.GetFileName(item)`，如果希望不要带扩展名的名称，可用 `System.IO.Path.GetFileNameWithoutExtension(item)`。

6. **Q：Split 分割字符串方法怎么使用？**

    **A：** 可参考 [如何在 C#中使用 String.Split 分隔字符串](https://docs.microsoft.com/zh-cn/dotnet/csharp/how-to/parse-strings-using-split)。

7. **Q：Json 字符串可以转数据表吗？**

    **A：** 可以使用 C#代码转换，具体可参见 [Json 转 DataTable](https://www.cnblogs.com/zhangjd/p/6007072.html)

## Excel 相关

1. **Q：为什么打开 WPS 文档，报错“[NPOI.POIXMLException--> System.Reflection.TargetInvocationException: 调用的目标发生了异常。”**

    ![WPS 异常](https://docimages.blob.core.chinacloudapi.cn/images/Studio/wpserror20210826.png)

    **A：** 需要在桌面右键文件，选择默认打开程序改成 Office，即可恢复正常。

2. **Q：如果没有安装 office，想要使用 office 组件，有办法吗？**

    **A：** 若可以安装 WPS，也可以用 office 组件，WPS 用的是 office 的库。

3. **Q：如何实现 EXCEL 行数不固定情况下的数据自动填充？**

    **A：** 使用“写入行/列数据”组件，使用“获取末行号”组件搭配数据确定要加几个，创建数组变量，要填几个数据，就加几个。

## 操作/逻辑相关

1. **Q：编辑器内撤销后是否能恢复?**
    **A：** 不能。

2. **Q：如何让机器人知道这里有几页，需要截几次图（每页截图 1 次）？**

    ![页面页数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/pages20210826.png)

    **A：** 获取这个标签的值 3 页，然后截取“3”，以后数据多了，获取了这个标签值也会随总数据量变化，可以做到动态。

3. **Q：区域截取是使用截屏组件吗？为什么会报错“发生了以下错误：截屏不支持图像识别”？**

    **A：** 区域截取建议使用“组件市场”中的组件，可以设置坐标范围。而“截屏”组件是根据元素截图，不支持按住 Ctrl 截取区域，您可以指定一个相对固定的元素然后设定大小和偏移。

4. **Q：在 Web 网站自动输入查询条件查询，为什么输入的条件不生效，Web 网站展示了所有数据？**

    **A：** 有些只能点击，有些可以用 JS，有些可以直接输入，所以需要根据实际情况判断使用哪种。如果手动输入方便，则先鼠标点击，获取焦点，然后再输入。

5. **Q：AI 识别到的是一个字符串内容，该怎么处理？**

    **A：** 返回是 json 格式的序列化后的字符串，可以用 JSON“反序列化”组件，也可以用字符串匹配来提取想要的内容。

6. **Q：把数据添加到 Oracle 数据库用什么组件？**

    **A：** 使用 [连接数据库](./../Activities/Database/ConnectDatabase.md) 组件。

7. **Q：如何往拼接好的 JSON 里循环追加数组？**

    **A：** 目前没有组件可以直接添加，可以在执行 C#代码组件中写代码处理。

8. **Q：无法获取 Excel 中的列头，报错“[错误] 列“发票代码”不属于表”，该如何解决？**

    ![列不属于表](https://docimages.blob.core.chinacloudapi.cn/images/Studio/row20211008.png)

    **A：** 使用 **读取区域** 组件，勾选“添加列头”选项。

9. **Q：如何实现滑动鼠标滚轮，让网页页面下拉？**

    **A：** 使用 **点击** 组件点击向下按钮，若操作不便可使用快捷键 pagedown 翻页。

## 手机自动化相关

参见 [手机自动化常见问题](../Studio/process/developProject/MobileDevicesManage/MFAQ.md)。

## 其他问题

1. **Q：RPC 服务器不可用，报错“Exception from HRESULT: 0x800706BA”，为什么会偶尔出现此错误？**

    **A：** 参见 [RPC 服务器不可用的解决方案](https://www.cnblogs.com/bosins/p/13150489.html)。

2. **Q：是否有 PPT VBA 自动化的资料？**

    **A：** 参见 [PowerPoint VBA(Macros)教程](https://zhuanlan.zhihu.com/p/134142512)。
