# FAQ

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

## 激活/许可证相关

1. **Q：编辑器许可证已过期，是否需要应用新的许可证？企业版的没联网是否就会出现此弹窗提示？**

    **A：** 没有网络无法使用社区版编辑器。联网激活企业版编辑器，使用也需要联网，许可证激活可以断网使用。

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

## 市场相关

1. **Q: 从组件市场安装的组件包存放在本地计算机什么路径下？**

   **A：** `%UserProfile%\.nuget\packages`

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

## 指定元素相关

1. **Q: 使用组件中的“指定元素”指定浏览器时，无法定位到目标应用程序，验证失败。**

    ![指定元素验证失败](https://docimages.blob.core.chinacloudapi.cn/images/Studio/locateelement20210603.png)

    **A：** 观察目标 title 的特征，如果目标 title 为动态的，把动态字段的值用*来代替。

2. **Q：有个流程每天运行，不定期会偶发某个组件元素定位失败，但调查问题组件无法再现问题，整体流程稳定性很差，是否有改进方法？（流程操作：桌面 CMS 程序，win10 系统）**

    **A：** 这与系统元素的响应时长有关，建议在出问题的组件上加延迟，或在此步骤前使用等待元素出现组件。
    一般有以下几种方式增加稳定性，增加超时时间、重试、机器人运行出错时截图，在使用前先等待元素出现。exe 应用程序出错时，建议排错期间先不要关闭，查看此时能否验证成功。

3. **Q：如何精确定位到 Excel 内的 button？**

    **A：** 录制技术切换至 IA。

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

4. **Q：这个同样的语句，为什么在另一个组件里面调试正常，到这里就报错？**

    ![类型转换错误](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeconverterror20210824.png)

    **A：** Substring(7,4) ，不是 SubString(7,4)，存在拼写错误。
