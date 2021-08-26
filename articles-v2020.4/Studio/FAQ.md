# FAQ

[toc]

## 安装相关

1. **Q：安装时弹出程序崩溃提示，如图：**

   ![安装崩溃](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/installCollapse.png)

   **A：** 打开控制面板-> 程序-> 卸载程序，在卸载或更改程序列表中检查是否安装.Net Framework 4.6.1 及以上版本的.Net Framework 环境。如果未安装，请先下载.Net Framework 4.6.1 并安装，安装好之后重启电脑再进行云扩 RPA 编辑器的安装。下载地址：<https://www.microsoft.com/zh-CN/download/details.aspx?id=49982>

2. **Q：点击安装，显示安装失败**

   ![安装失败](https://docimages.blob.core.chinacloudapi.cn/images/Studio/installfailed20210824.png)

    **A：**

    - 排查步骤 1：检查杀毒软件是否正在运行，关闭杀毒软件后重新安装。

    - 排查步骤 2：检查当前用户在安装目录的读写权限，如果当前用户在安装路径没有读写权限，则要用管理员账号登录，在安装目录右键，点击属性，点击安全标签，添加目标账户，并添加完全控制权限，最后点击确定，然后退出管理员账号，用目标用户登录进行安装。

3. **Q：编辑器的默认安装目录是什么？**

    **A：** `%UserProfile%\AppData\Local\Encoo Studio`

4. **Q：已安装机器人后安装编辑器，报错“错误消息：未将对象引用设置到对象的实例”。**

    ![安装报错](https://docimages.blob.core.chinacloudapi.cn/images/Studio/studioinstallerror20210825.png)

    **A：** 可检查是否安装“.net 中文语言包”，如果安装了，可以卸载后再尝试，如果没有安装，可检查日志。

    ![中文语言包](https://docimages.blob.core.chinacloudapi.cn/images/Studio/dnetpackage20210825.jpg)

## 激活/许可证相关

1. **Q：编辑器许可证已过期，是否需要应用新的许可证？企业版的没联网是否就会出现此弹窗提示？**

    **A：** 没有网络无法使用社区版编辑器。联网激活企业版编辑器，使用也需要联网，许可证激活可以断网使用。

2. **Q：编辑器登录时无法激活，提示“没有可用的许可证”，是什么原因？换了电脑后如何解绑？**

    **A：** 社区版只有一个 RPA 编辑器可以使用， 确认是否已激活一个编辑器了？可登录控制台，点击“许可证” 菜单，进行解绑。

    ![许可证](https://docimages.blob.core.chinacloudapi.cn/images/Studio/license20210825.png)

## 卸载相关

1. **Q：卸载失败**

   **A：** </br>
   (1) 安装目录(Program files x86)，25 版本以后的安装目录在用户目录 AppData\Local\，下面 encootech 文件夹删掉 </br>
   (2) C:\ProgramData\Package Cache\ 里面搜一下 Digi4th 开头的 都删掉 </br>
   (3) 删除 windows 服务 DataBusService(cmd 命令行 sc delete DataBusService)

## 系统日志相关

1. **Q：编辑器的系统日志的默认路径是什么？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Log`。

2. **Q：编辑器的安装日志的默认路径是什么？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Installation`。

## 项目相关

1. **Q: 建了两个项目，如何才能把两个项目合并，使得打开编辑器时两个都可以看到？**

    **A：** 可在需要保留的项目中把另外一个项目的 xaml 文件都导入过去。

    ![导入文件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Importproject20210824.png)

2. **Q：新建了一个项目，报错：[错误] 未能从程序集“BotTimeUI.Common, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null”中加载类型“BotTimeUI.Common.Utility.ChildrenAccessWay”。**

    **A：** 如果是新安装的编辑器，可能是和其他版本冲突了。先关闭编辑器，在 `C:\users\<user>\.nuget` 下面，将 packages 文件夹重命名，相当于备份，然后重新打开编辑器，新建项目。

## 调试/运行相关

1. **Q：如何执行项目下其他的 xaml 文件，按 F5 编辑器默认从 Main.xaml 执行。**

    **A：** 右键点击有执行快捷键：`F6` 可调试当前打开的流程，`Ctrl+F6` 可运行当前打开的流程。

2. **Q：通过设置断点调试流程，是否指运行到断点就停止了？如果需要恢复应该如何操作？**

    **A：** 断点只是调试用的，不影响运行，停下后在左侧面板点击“继续”还会继续往下跑的。如果需要恢复，右击“删除断点”即可。

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

## 插件相关

1. **Q: Chrome 录制失败，自动化失败有哪些原因？**

    **A：** </br>
    (1) 检查 chrome 浏览器扩展，是否安装了 chrome 插件并且启用，如图：

    ![启用扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/chrome-usingExtension.png) </br>

    (2) 当打开 chrome 后，检查任务管理器是否存在进程：EncooNativeMessageHost.exe，该进程是 RPA 与 chrome 浏览器的通信进程，如果不存在，则检查(1)。

    ![检查进程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/taskManager.png) </br>

2. **Q: 怎么安装 chrome 插件？**

    **A：** 打开编辑器，在 **开始 > 工具 > 扩展** 中，选择并点击“Chrome 扩展”，根据提示操作即可。（在安装后，请手动打开浏览器并输入：chrome://extensions/，启用扩展。）

    ![安装扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/extensioninpath20201019.png)

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

## 指定元素/选择器相关

1. **Q: 使用组件中的“指定元素”指定浏览器时，无法定位到目标应用程序，验证失败。**

    ![指定元素验证失败](https://docimages.blob.core.chinacloudapi.cn/images/Studio/locateelement20210603.png)

    **A：** 观察目标 title 的特征，如果目标 title 为动态的，把动态字段的值用*来代替。

2. **Q：有个流程每天运行，不定期会偶发某个组件元素定位失败，但调查问题组件无法再现问题，整体流程稳定性很差，是否有改进方法？（流程操作：桌面 CMS 程序，win10 系统）**

    **A：** 这与系统元素的响应时长有关，建议在出问题的组件上加延迟，或在此步骤前使用等待元素出现组件。
    一般有以下几种方式增加稳定性，增加超时时间、重试、机器人运行出错时截图，在使用前先等待元素出现。exe 应用程序出错时，建议排错期间先不要关闭，查看此时能否验证成功。

3. **Q：如何精确定位到 Excel 内的 button？**

    **A：** 录制技术切换至 IA。

4. **Q：在浏览器上点击链接打开新的浏览器窗口，运行的时候新窗口上的内容一直不能正常执行，总是报错: 操作已超时。**

    **A：** 可能是新窗口上的元素没定位成功，需检查定位的元素里有哪些可能是动态变化的。在选择器编辑器中把可能发生变化的部分用 `*` 代替。

    ![选择器编辑器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/selector20210825.png)

5. **选择器中是否可以写变量？**

    **A：** 可以的，`{{变量名}}`。

## 操作相关

1. **Q：编辑器内撤销后是否能恢复?**
    **A：** 不能。

2. **Q：编辑器流程中的组件未显示，报错“未能生成 BrowserOpen 的视图”。**

    **A：** 按照如下步骤进行处理：

    - step1: 关闭编辑器
    - step2：在文件资源管理器输入目录：`%userprofile%\.nuget\packages\automationactivity`，然后重命名此文件夹，如 `automationactivity01`
    - step3：重启编辑器

3. **Q：String 类型如何转化为 int？**

    **A：** Convert.ToInt32("String 字串")。

4. **Q：如何用变量计算时间差？比如从网页上获取了一个文本，转换为时间格式后，如何计算时间和自己当前操作时间的时间差？**

    **A：** 可参见 [C#日期加减](https://www.cnblogs.com/RCJL/p/12930425.html?wework_cfm_code=OTcx9KzwohAgedF7GMK4w2wgfzzAnXYvJkWj%2BfQlKu2ufHEl5IWDPUfA5BGsjcdX02a8d5HRYX8WgPkozEyQ1Q7DOODUJ1%2F2Iej2z%2FE1Bpbs4YNG7XGzAoI%3D)。

5. **Q：字符串中如果包含双引号，是否可以使用转义字符？**

    **A：** 可以，两个双引号代表一个双引号。

6. **Q：这个同样的语句，为什么在另一个组件里面调试正常，到这里就报错？**

    ![类型转换错误](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeconverterror20210824.png)

    **A：** Substring(7,4) ，不是 SubString(7,4)，存在拼写错误。

7. **Q：区域截取是使用截屏组件吗？为什么会报错“发生了以下错误：截屏不支持图像识别”？**

    **A：** 区域截取建议使用“组件市场”中的组件，可以设置坐标范围。而“截屏”组件是根据元素截图，不支持按住 Ctrl 截取区域，您可以指定一个相对固定的元素然后设定大小和偏移。

8. **Q：在 Web 网站自动输入查询条件查询，为什么输入的条件不生效，Web 网站展示了所有数据？**

    **A：** 有些只能点击，有些可以用 JS，有些可以直接输入，所以需要根据实际情况判断使用哪种。如果手动输入方便，则先鼠标点击，获取焦点，然后再输入。

## 其他问题

1. **Q：RPC 服务器不可用，报错“Exception from HRESULT: 0x800706BA”，为什么会偶尔出现此错误？**

    **A：** 参见 [RPC 服务器不可用的解决方案](https://www.cnblogs.com/bosins/p/13150489.html)。

2. **Q：是否有 PPT VBA 自动化的资料？**

    **A：** 参见 [PowerPoint VBA(Macros)教程](https://zhuanlan.zhihu.com/p/134142512)。
