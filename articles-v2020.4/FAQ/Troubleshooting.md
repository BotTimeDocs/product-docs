# 异常报错排查

## 一、报错-信息索引

### 1.1 控制台-报错索引

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1|未知异常|控制台机器人激活|C0001
2|机器人未授权，请在控制台绑</br>定许可后重新连接  |控制台机器人激活|C0002
3|服务器内部异常|控制台机器人激活|C0003

### 1.2 编辑器、机器人-报错索引

#### （1）编辑器/机器人/插件扩展_安装、激活

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1| 此应用无法在你的电脑上运行 |编辑器安装|I0001
2| 未将对象引用设置到对象的实例 |编辑器安装|I0002
3| 这计算机中已经安装了.NET </br>Framework </br>4.6.1(简体中文)或版本更高的更新 |编辑器安装|I0003
4| [Installation has failed]</br>There was an error while installing</br> the application.Check</br> the setup log for more information </br>and contact the author |编辑器安装|I0004
5| [Installation has failed]</br> Failed to install</br>the .NET Framework,try installing the</br> latest version manually |编辑器安装|I0005
6| Value cannot be null.</br>Parameter name:path1|编辑器安装 |I0006
7| 该许可证不能在当前计算机上注册|编辑器本地激活 |I0007
8| Java扩展安装失败! |扩展安装|E0001
9| 检测到Java应用程序,</br>请更新Java插件 |扩展安装|E0002
10| 无效许可提示 |激活机器人|R0001
11| 尚未安装.Net Framework 4.6.2,</br>原因是：时间戳签名和/或</br>证书无法验证或已损坏 |编辑器安装|I0008


#### (2)Excel/Office自动化
|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1|0x80070057|环境_三方软件冲突、筛选|AC0001
2|0x80029C4A|环境_加载类型库/DLL|AC0002
3|0x80004002 |环境_COM类相关|AC0003
4|检索 COM 类工厂中 CLSID 为</br> {00021A20-0000-0000</br>-C000-000000000046} </br>的组件时失败， 0x80080005|环境_COM类相关|AC0004
5|0x80040154|环境_COM类相关|AC0005
6|0x8001010A |运行_可视|AC0006
7|0x80010105|打开/新建|AC0007
8|0x800A03EC|打开/新建|AC0008
9|0x8002801D|打开/新建|AC0009
10|定时任务，0x80080005|打开/新建|AC0010
11|0x8007065E|打开/新建|AC0011
12|0x800A03EC|写入单元格|AC0012
13|0x8002000A|写入单元格|AC0013
14|0x800A01A8|读取区域|AC0014
15|0x800706BA|执行宏|AC0015
16|0x800A03EC|执行宏|AC0016
17|0x8FE3301F|创建透视表|AC0017
18|加载类型库/DLL 时出错|打开/新建|AC0018
19|Excel尚未安装|打开/新建|AC0019
20|文件扩展名不正确|打开/新建|AC0020
21|OPC Compliance error [M4.3]|读取单元格、读取区域|AC0021
22|输入区域无效|读取区域|AC0022
23|类Range的AutoFilter方法无效|筛选|AC0023
24|RPC 服务器不可用|执行宏|AC0024
25|不信任到Visual Basic Project的程序连接|执行宏|AC0025
26|类 PivotTable 的 PivotFields 方法无效|筛选|AC0026
27|不支持给定路径的格式|新建文件/文件夹|AC0027
28|Your stream was neither</br> an OLE2 stream, nor an OOXML stream.|打开/新建|AC0028
29|指定的参数已超出有效值的范围|排序|AC0040

#### (3)元素定位/(界面&手机)自动化

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1|元素不支持通过设置控件的方式点击|点击|AA0001
2|定位元素超时|点击|AA0002
3|打开浏览器失败。the operation has timed out|浏览器|AA0003
4|所请求的剪贴板操作失败。|剪贴板、复制粘贴|AA0004
5|用户回调引发异常|网银登录界面|AA0005
6|句柄无效|网银登录界面|AA0006
7|云扩录制器奔溃了|私有化环境、权限问题|AA0007
8|不能根据选择器获取窗体|指定元素|AA0008
9|Bitbit调用失败Error:6|截屏、远程桌面|AA0009
10|打开浏览器失败|浏览器|AA0010
11|Poco Service服务启动异常|手机自动化|AA0011

#### (4)数据表/数据库自动化

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1|error 0: Authentication to host</br> 'localhost' for user 'root' using method</br> 'caching_sha2_password' failed </br>with message: Reading from </br>the stream has failed|Mysql、连接数据库|AC0030
2|Loading local data is disabled; </br>this must be enabled on both </br>the client and server sides|Mysql、连接数据库|AC0031
3|无法加载DLL“db2app.dll”：</br>找不到指定的模块</br>（异常来自HRESULT：0x8007007E）|Db2、连接数据库|AC0032
4|连接已经是本地事务处理</br>或分布式事务处理的一部分|连接数据库|AC0033

#### (5)邮件自动化

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1|获取邮件信息失败|获取邮件|AC0034
2|发送邮件失败。535: Login Fail. </br>Please enter your authorization code to login. |发送邮件|AC0035
3|连接服务器失败|发送邮件|AC0036
4|[错误]Outlook的COM端口被占用，</br>请检查是否有插件占用改端口</br>或者关闭Outlook客户端。|发送邮件|AC0037

#### (6)其他异常报错(系统组件、远程、流程执行…)

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1|call remote method timeout,method name :</br> invokeRemoteUiObjectAsync |远程桌面断开|AC0038
2|Data descriptor signature not found|解压缩文件|AC0039
3|请检查是否已安装机器人并处于正常运行状态|流程发布时|I0009
4|服务未正常启动，请尝试手动启动服务或重启电脑|流程发布时|I0010
5|未检测到服务，可能被其他软件卸载|流程执行时|R0002
6|原因：拒绝访问|流程执行时|R0003
7|[Error] 未能转换部分或所有标识引用|流程执行时|R0004
8|活动"Encooworkflow.Main"的CacheMetadata</br>引发了"System.Xaml.</br>XmalObjectWriterException":</br>无法设置未知成员…… 请确认相关的组件</br>是否包含在nuget目录下|打开流程包|R0005
9|“HTTPSConnectionPool</br>(host='digpro.ininin.com', port=443): </br>Max retries exceeded with url: </br>/dpsthird/api/v1/production/</br>save_or_update</br> (Caused by NewConnectionError</br>('<urllib3.connection.HTTPSConnection </br>object at 0x000001DAA66E4640>:</br> Failed to establish a new connection:</br> [Errno 11001] getaddrinfo failed'))”|流程执行时|R0006
10|未能生成XXX视图|打开流程包|I0011
11|此组件缺失，或无法正常加载|打开流程包|I0012
12|[错误] 类型XXX的对象无法转换为类型XXX|打开流程包|I0013
13|[错误]  Method not found…|打开流程包|I0014
14|[错误] Main.xaml: “对类型“……”</br>的构造函数执行符合指定的</br>绑定约束的调用时引发了异常。”，</br>行号为“XXX”，行位置为“XXX”。</br> 行：XXX, 列：XX|打开流程包|I0015
15|[错误]活动“登录”的CacheMeta </br>引发了"System.Xaml.……:</br>无法创建未知类型"{XXX}……"。</br>请确认相关的组件包</br>是否包含在nuget目录下"|打开流程包|I0016

## 二、具体报错-解决办法


### 2.1 控制台

#### 【报错异常】 V3版本控制台，机器人激活显示：未知异常。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/解决办法-C0001.png)</br>
<font color=5a6877>
</br>**【解决办法-C0001】**：控制台版本有点老，Encoo.Robot.Service.exe.config和Robot.exe.config都加一段<add key="ConsoleVersion" value="V3"/>
然后把robot.exe和服务都重启了，那两个文件在C:\Program Files (x86)\Encoo Robot\app-1.1.2204.10下，服务名称叫encoo robot service。
</font>

<font color= grey>*PS：为了后续更好体验控制台功能 享受其他版本升级服务，您可以联系商务沟通控制台升级*</font>
</br></br>
---
</br>

#### 【报错异常】 使用控制台账号激活机器人时报错“机器人未授权，请在控制台绑定许可后重新连接”</br>
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/C0002.png)</br>

<font color=5a6877>
</br>**【解决办法-C0002】**：确认该连接字符串是否为控制台“机器人管理”中创建的机器人对应的“机器人连接字符串”。</br>
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/C0002-2.png)
</font>

</br></br>
---
</br>

#### 【报错异常】使用控制台账号激活机器人时，报错“服务器内部异常”
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/C0003.png)

<font color=5a6877>
</br>**【解决办法-C0003】**：
1. 确认近期控制台是否有升级操作；
2. 如果是控制台有升级，机器人版本未升级导致的话，可以手工copy这个dll文件到，`C:\Program Files (x86)\Encoo Robot\<app-1.1.2xxx.x> `下面试试看，copy前备份原来的dll，然后重启机器人服务。

</font></br></br>
---
</br>


### 2.2 编辑器/机器人/插件扩展_安装、激活

####【报错异常】此应用无法在你的电脑上运行
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-1.png)

<font color=5a6877>
</br>**【解决办法-I0001】**
* Step1、确认一下【计算机配置】—【Windows设置】—【安全设置】—【本地策略】—【安全选项】 已经启用了用户账户控制：以管理员批准模式运行所有管理员…… 
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-3.png)

</br>

* Step2、如果上一步还是不行，那安装包可能被串改了，重新下载一个安装包吧，注意安装的时候 关闭一下 杀毒软

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0001-4.png)

</font></br></br>
---
</br>

####【报错异常】未将对象引用设置到对象的实例
* 编辑器安装时，显示发生了以下错误，错误信息：未将对象引用设置到对象的实例

</br>

<font color=5a6877>
**【解决办法-I0002】**编辑器安装失败确认排查步骤如下 ：
- Step1：检查杀毒软件是否正在运行，关闭杀毒软件(如，360 软件)后重新安装。
- Step2：可在控制面板中，检查是否安装“.net 中文语言包”，如果安装了，可以卸载后再尝试，如果没有安装，可检查日志。卸载后若没安装.net去下载安装一下对应的的英文版安装包，具体选项示例如下方所示

</font></br></br>
---
</br>


####【报错异常】这计算机中已经安装了.NET Framework 4.6.1(简体中文)或版本更高的更新
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0003.png)

<font color=5a6877>
</br>**【解决办法-I0003】**
* 如果重新安装.NET Framework依然失败提示同样错误信息，那么需要清理注册表
Software\Microsoft\Windows\CurrentVersion\Uninstall\Microsoft .NET Framework 4 Client Profile CHS Language Pack

</font></br></br>
---
</br>

####【报错异常】[Installation has failed]There was an error while installing the application.Check the setup log for more information and contact the author

<font color=5a6877>
</br>**【解决办法-I0004】**编辑器安装失败确认排查步骤如下 ：
* Step1：检查杀毒软件是否正在运行，关闭杀毒软件(如，360 软件)后重新安装。
* Step2：检查当前用户在安装目录的读写权限，如果当前用户在安装路径没有读写权限，则要用管理员账号登录，在安装目录右键，点击属性，点击安全标签，添加目标账户，并添加完全控制权限，最后点击确定，然后退出管理员账号，用目标用户登录进行安装。

</font></br></br>
---
</br>

####【报错异常】[Installation has failed] Failed to install the .NET Framework,try installing the latest version manually

<font color=5a6877>
</br>**【解决办法-I0005】**robot运行是基于.net环境的，如果是win7操作系统，则需要手动安装下.net插件，可以通过离线包安装

</font></br></br>
---
</br>

####【报错异常】Value cannot be null.Parameter name:path1

<font color=5a6877>
</br>**【解决办法-I0006】**开启杀毒软件导致的，关闭后重新安装就好了
</font></br></br>
---
</br>

####【报错异常】该许可证不能在当前计算机上注册|本地许可证激活

<font color=5a6877>
</br>**【解决办法-I0007】**
请联系商务确认是否许可证不对，若不对重新购买或申请许可证
</font></br></br>
---
</br>

####【报错异常】Java扩展安装失败!
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/E0001.png)

<font color=5a6877>
</br>**【解决办法-E0001】**
- 有网络情况 —— 登录编辑器之后再按照 
- 无网络离线情况 —— 参考手动安装扩展，具体参考链接:(待补充)

</font></br></br>
---
</br>

####【报错异常】检测到Java应用程序,请更新Java插件

<font color=5a6877>
</br>**【解决办法-E0002】**
- 第一步 ：更新Java拓展 
- 第二步：若还是不行，继续弹这个提示，禁用默认jab, jre bin目录下有个jabswitch.exe.
cmd 执行 “jabswitch.exe -disable”

</font></br></br>
---
</br>

####【报错异常】无效许可提示|激活机器人
* 机器人激活许可证时候，之前可以正常激活，重新卸载激活机器人报"无效许可提示"
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0001.png)

<font color=5a6877>
</br>**【解决办法-R0001】**
* 首先确认电脑系统无重装，且无更换电脑或服务器后确认。
* 然后确认前后使用许可的机器人安装包版本是否一致 。
</font></br></br>
---
</br>

#### 【报错异常】尚未安装.Net Framework 4.6.2,原因是：时间戳签名和/或证书无法验证或已损坏
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0008.png)
<font color=5a6877>

【原因分析】
1. 问题描述：不受信任的证书 —— 原因：证书未安装
2. 问题描述：时间戳签名和/或证书无法验证或已损坏 —— 原因：系统版本太老

</br>**【解决办法-I0008】**

1. 解决方法：MicrosoftRootCertificateAuthority2011.cer 去网上下载此证书点击安装即可

2. 解决方法：安装KB2813430补丁；    
    * [32位系统补丁下载地址（点击下载)](https://www.microsoft.com/zh-CN/download/details.aspx?id=39110)
    * [64位系统补丁下载地址](https://www.microsoft.com/zh-CN/download/details.aspx?id=39115)

补充：[推荐相关阅读-(点击查看)](https://blog.csdn.net/wl_tian_dao_chou_qin/article/details/123002341?ops_request_misc=&request_id=&biz_id=102&utm_term=%E6%97%B6%E9%97%B4%E6%88%B3%E7%AD%BE%E5%90%8D%E5%92%8C%E6%88%96%E8%AF%81%E4%B9%A6&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-123002341.142^v13^pc_search_result_control_group,157^v14^new_3&spm=1018.2226.3001.4187)


</font >

</font></br></br>
---
</br>


### 2.3 Excel/Office自动化
 <font color=grey size=2 > 
> RPA流程自动化中，Office自动化操作需要官方excel软件,
> 请注意不要使用 <font color=black size=2 >**非官方破解、绿色等**</font>版本非官方版本软件(其接口**不支持**)；
> 另外WPS或Office未安装好、或者Office或WPS版本冲突导致现象导致的异常,
> 需要对Office/WPS软件进行修复。
> </font>

#### 【报错异常】加载类型库/DLL 时出错。 (Exception from HRESULT: 0x80029C4A (TYPE_E_CANTLOADLIBRARY)) 

<font color=5a6877>
</br>**【解决办法-AC0018-1】**：如下 
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0018-1.png)
</br>**【解决办法-AC0018-2】**：从[官方下载](https://support.microsoft.com/zh-cn/office/%E4%BB%8E-pc-%E5%8D%B8%E8%BD%BD-office-9dd49b83-264a-477a-8fcc-2fdf5dbf61d8)Office完全卸载工具
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0018-2.png)
</br>**【解决办法-AC0018-3】**：使用Office Tool工具卸载，链接：[Office Tool Plus 官方网站](https://otp.landian.vip/zh-cn/)
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0018-3.png)
</font></br></br>
---
</br>

#### 【报错异常】0x80070057 (E_INVALIDARG))

<font color=5a6877>
</br>**【解决办法-AC0001】**：检查是否同时安装wps和office，并且将wps设置为默认程序，如果是卸载wps即可；
</font></br></br>
---
</br>


#### 【报错异常】检索 COM 类工厂中 CLSID 为 {00021A20-0000-0000-C000-000000000046} 的组件时失败，原因是出现以下错误: 0x80080005

<font color=5a6877>
</br>**【解决办法-AC0004】**：除用工具彻底卸载wps或Office外,如果下图所示注册表,也整个删除
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0004.png)



</font></br></br>
---
</br>


#### 【报错异常】环境_COM类相关，报错信息：0x80004002 
无法将类型为“System.__ComObject”的 COM 对象强制转换为接口类型“Microsoft.Office.Interop.Excel.Worksheet”。此操作失败的原因是对 IID 为“{000208D8-0000-0000-C000-000000000046}”的接口的 COM 组件调用 QueryInterface 因以下错误而失败: 不支持此接口 (异常来自HRESULT:0x80004002 (E_NOINTERFACE))。

【问题原因】：电脑安装先后多个Office Excel版本，或者安装过WPS。

<font color=5a6877>
</br>**【解决办法-AC0003】**：
* 在注册表中找到：
HKEY_CLASSES_ROOT\TypeLib\{00020813-0000-0000-C000-000000000046}
在其子项中，删除与当前Excel版本不一致的选项即可。
注意：删除注册表选项前，请先备份删除的选项。
如下图所示：
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0003.png)
</font></br></br>
---
</br>


#### 【报错异常】详细错误信息：检索COM类工厂中CLSID为{00024500-0000-0000-C000-000000000046}的组件失败，原因是出现以下错误：80040154没有注册类（异常来自HRESULT:0x80040154(REGDB_E_CLASSNOTREG))。

<font color=5a6877>
【原因分析】：在操作系统中注册的COM组件的多个版本（WPS/Excel）弄乱了
</br>**【解决办法-AC0005】**：[点击查看链接：COM类错误80040154](https://blog.csdn.net/cxygs5788/article/details/106351373?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2.pc_relevant_default&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2.pc_relevant_default&utm_relevant_index=5)
</br></br>
**补充：如何修复对应的WPS和office365？**</br>
* WPS COM 如何修复？</br>
</br>【解决办法】：解决方式如下，即用修复工具修复一下 ，WPS用对应WPS的配置工具，WPS修复示意图：</br>

![-w300](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/WPS-修复.png)![-w300](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/WPS修复-1.png)
</br></br>
* Office 365 如何修复？

</br>【解决办法】：解决方式如下，即用修复工具修复一下 ，Office 365用自带修复方案 </br>

![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/365修复-1.png)
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/365-2.png)

</font></br></br>
---
</br>


### 2.2 EXCEL-打开新建

#### 【报错异常】详细错误信息：Excel尚未安装. 

<font color=5a6877>
</br>**【解决办法-AC0019】**：
* 可能是wps安装的问题，你可以试下打开新建组件，切换运行环境为无依赖。
</br>
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0019-2.png)

</br>
* 运行的时候 设置一下 这个 别选 管理员运行 ，WPS第三方不支持管理员 或者要管理员必须就建议按照office excel。

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0019-1.png)
</br>*补充：wps是per user 安装，不能用管理员运行。 以上办法都不行时，试一下官方工具卸载之后重装WPS或Office*

</font></br></br>
---
</br>


#### 【报错异常】WPS“打开/新建”-打开.xlsm文件报错，[错误]文件扩展名不正确
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0020.png)
<font color=5a6877>
【原因分析】：
● .xlsm格式是只支持在excel里面打开，wps不支持

● 编辑器1.1.2204.9版本开始，合并excel和WPS分类，“打开/新建”合并为一个，新版本功能不会再出现此类问题报错。

</br>**【解决办法-AC0020】**：
用excel-打开/新建 ，替换掉wps-打开/新建

</font></br></br>
---
</br>


#### 【报错异常】打开/新建失败，错误代码：0x80010105(RPC_E_SERVERFAULT)

<font color=5a6877>
</br>**【解决办法-AC0007】**：检查是否安装福昕PDF阅读器，找到“excel选项”，点开后点击“加载项”，最下面有个管理加载项的下拉菜单，选“COM加载项”，点“转到”，这时会弹出一个框，把里面pdf软件的加载项前面的勾去掉，点确定；

</font></br></br>
---
</br>

#### 【报错异常】打开/新建 HRESULT E_FAIL，报错信息：0x800A03EC

<font color=5a6877>
</br>**【解决办法-AC0008】**：检查文件是否能正常打开，导致的原因有多种，一般是由于该EXCEL文件的编辑环境发生较大变化，如64位系统环境下编辑的EXCEL不一定能在32位系统环境下顺利读取。

</font></br></br>
---
</br>


#### 【报错异常】打开/新建失败，报错信息：0x8002801D

详细错误信息：Unable to cast COM object of type 'Microsoft.Office.Interop.Excel.ApplicationClass' to interface type 'Microsoft.Office.Interop.Excel._Application'. This operation failed because the QueryInterface call on the COM component for the interface with IID '{000208D5-0000-0000-C000-000000000046}' failed due to the following error: 库没有注册。 (Exception from HRESULT: 0x8002801D (TYPE_E_LIBNOTREGISTERED)).

<font color=5a6877>
</br>**【解决办法-AC0009】**：排查电脑是否安装过wps,如 是:重新安装wps

</font></br></br>
---
</br>


#### 【报错异常】打开/新建失败。详细错误信息：Retrieving the COM class factory for component with CLSID {00024500-0000-0000-C000-000000000046} failed due to the following error: 8007065e 这个类型的数据不受支持。 (Exception from HRESULT: 0x8007065E).

<font color=5a6877>
【原因分析】：安装的Excel版本不正确

</br>**【解决办法-AC0011】**：[点击查看：CLSID 为 {00024500-0000-0000-C000-000000000046} 的组件失败](https://blog.csdn.net/weixin_34293911/article/details/94269260?ops_request_misc=&request_id=&biz_id=102&utm_term=0x8007065E&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-94269260.nonecase&spm=1018.2226.3001.4187)

</font></br></br>
---
</br>


#### 【报错异常】定时任务，打开/新建失败，HRESULT:0x80080005
【原因分析】：如果许多 COM+ 应用程序在 This User 属性中指定的不同用户帐户下运行，则计算机无法分配内存以创建新用户的新桌面堆。 因此，进程无法启动。

<font color=5a6877>
</br>**【解决办法-AC0010】**：具体解决办法,详见链接：[启动多个 COM+ 应用程序时出错：错误代码80080005 -- 服务器执行失败](https://docs.microsoft.com/zh-cn/troubleshoot/windows-server/application-management/error-8008005-when-start-complus-applications)

</font></br></br>
---
</br>


#### 【报错异常】OPC Compliance error [M4.3]：Producers shall not create a document element that contains refinements to the Dublin Core elements，except tor the two specified in the schema：

<font color=5a6877>
【原因分析】：Excel兼容性导致

</br>**【解决办法-AC0021】**：点击查看链接[使用poi读取excel异常](https://blog.csdn.net/IM507/article/details/100561304)，参考链接内容看下应该是否文件有问题，可以把打开失败的文件名抛出，整理成一个列表比那与之后查看

</font></br></br>
---
</br>

### 2.3 Excel-读取写入

#### 【报错异常】excel 超出当前范围。 (异常来自 HRESULT:0x8002000A (DISP_E_OVERFLOW))，excel 某些单元格格式有问题，读取就会有异常
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0013.png)
<font color=5a6877>
</br>**【解决办法-AC0013】**：定位不到错误行的情况下，可以全选把单元格格式都设为文本

</font></br></br>
---
</br>


#### 【报错异常】读取区域失败 ，错误示例“详细错误信息：A1：L1输入区域无效”

<font color=5a6877>
</br>**【解决办法-AC0022】**：确认一下，区域表示的“冒号”用了中文冒号，需要使用英文冒号

读取区域失败，详细错误信息：以下方法或属性之间的调用具有二义性：
“System.Data.DataRowColection.Add(System.Data.DataRow)”和“System.Data.DataRowCollection.Add(params object[])”
【解决办法】：可以试试把参数类型改成DataRow，然后看下哪里用的object[]

</font></br></br>
---
</br>

#### 【报错异常】读取区域失败，[错误] Exception from HRESULT:0x800A01A8
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0014.png)
<font color=5a6877>
</br>**【解决办法-AC0014】**：获取文件夹类别，一个个打开excel处理完关闭的时候，前面excel还没关闭好，进程被占用，前面打开加一个延时

</font></br></br>
---
</br>


#### 【报错异常】写入单元格失败，0x800A03EC。

<font color=5a6877>
</br>**【解决办法-AC0016】**：检查写入单元格是否合法超出excel范围


</font></br></br>
---
</br>


#### 【报错异常】工作表筛选_筛选出错，[错误]类Range的AutoFilter方法无效
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0023.png)
<font color=5a6877>
</br>**【解决办法-AC0023】**：报错与组件的全局筛选冲突  解决办法:在excel里先取消筛选

</font></br></br>
---
</br>


#### 【报错异常】使用筛选组件失败，且电脑只安装Wps，错误: 0x80070057

<font color=5a6877>
【原因分析】：Wps接口实现Office接口兼容性问题，若只安装Office情况能正常执行；

</br>**【解决办法-AC0001】**：按照下方的在步骤操作确认

1. 设置第二个筛选条件和第一个一样；
2. 更新编辑器版本，最新版本已经做了兼容性处理；

</font></br></br>
---
</br>


### 2.4 Excel-执行宏

#### 【报错异常】执行宏失败，错误代码：RPC 服务器不可用。 (异常来自 HRESULT:0x800706BA)

<font color=5a6877>
</br>**【解决办法-AC0015】**：检查宏脚本是否可以在excel中手动调用，其次检查宏函数名字是否以譬如set等关键字开头；

</font></br></br>
---
</br>


#### 【报错异常】执行宏失败。详细错误信息：不信任到Visual Basic Project的程序连接

<font color=5a6877>
</br>**【解决办法-AC0025】**：</br>

![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0025.jpg)

</font></br></br>
---
</br>


#### 【报错异常】执行宏失败。详细错误信息：0x800A03EC

<font color=5a6877>
</br>**【解决办法-AC0016】**：vba脚本问题

</font></br></br>
---
</br>


#### 【报错异常】执行宏 - 添加链接失败。详细错误信息：Exception from HRESULT: 0x800A03EC

<font color=5a6877>
【原因分析】：写入单元格超出合法excel范围了

</br>**【解决办法-AC0012】**：需要确认一下是不是行号或者列号是不是有错误，也有可能是宏文件本身无法打开

</font></br></br>
---
</br>


### 2.5 Excel-其他报错

#### 【报错异常】环境_COM类相关，报错信息：0x8001010A (RPC_E_SERVERCALL_RETRYLATER)

<font color=5a6877>
</br>**【解决办法-AC0006】**：详见链接，关掉可视 [c# - Error:-(Exception from HRESULT: 0x8001010A (RPC_E_SERVERCALL_RETRYLATER)) - Stack Overflow](https://stackoverflow.com/questions/26073754/error-exception-from-hresult-0x8001010a-rpc-e-servercall-retrylater)

</font></br></br>
---
</br>


#### 【报错异常】创建透视数据表失败，详细错误信息：类 PivotTable 的 PivotFields 方法无效

<font color=5a6877>
</br>**【解决办法-AC0026】**：要根据创建透视表数据源区域重新算列索引</br>
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0026.png)
</font>
</br></br>
---
</br>

#### 【报错异常】新建文件/文件夹失败，详细错误信息：不支持给定路径的格式。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0027.png)
<font color=5a6877>
</br>**【解决办法-AC0027】**：
系统-文件下的组件，如果出现报错"不支持给定路径的格式"时，一般是传入的路径的字符串开头存在一个不可见的字符，可以通过string.TrimStart(string[0])的方式来移除掉

</font>
</br></br>
---
</br>

#### 【报错异常】Your stream was neither an OLE2 stream, nor an OOXML stream.

<font color=5a6877>
【原因分析】：文件有问题,重命名过或者本身格式不对
</br>**【解决办法-AC0028】**：修复文件或者换一个文件试试

</font>
</br></br>
---
</br>

####【报错异常】写入区域失败。详细错误信息：无法对多重选择区域执行此操作

<font color=5a6877>
</br>**【解决办法-AC0029】**：确认excel表格是否有合并单元格，有的话取消之后再进行写入操作。

</font>
</br></br>
---
</br>

####【报错异常】排序失败。详细错误信息：指定的参数已超出有效值的范围
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0040.png)
<font color=5a6877>
</br>**【解决办法-AC0040】**：确认excel表格列头里面,是不是有合并单元格。
</font>
</br></br>
---
</br>


### 2.4 元素定位/(界面&手机)自动化

#### 【报错异常】使用图像识别定位的元素不支持通过设置控件的方式点击。

<font color=5a6877>
</br>**【解决办法-AA0001】**：图像识别方式定位元素的，点击方式选择模拟鼠标。

</font>
</br></br>
---
</br>

#### 【报错异常】定位元素超时

<font color=5a6877>
</br>**【解决办法-AA0002】**：定位元素超时可能存在一下几个原因，请注意排查确认
1. 选择器是否能验证到对应的元素？不会请先学习了解选择器：[入门006-选择器进阶课程](待补充)
2. 如果以上都没问题，可能是网络加载慢问题，请加长匹配超时的时间，具体参考点击组件使用说明文档：[点击组件](待补充)
3. 是否安装了对应的浏览器插件或其它扩展插件并启用？（安装过程关掉杀毒软件）

</font>
</br></br>
---
</br>

#### 【报错异常】打开浏览器失败。the operation has timed out

<font color=5a6877>
</br>**【解决办法-AA0003】**：一般情况下 ，首先请确认是否安装了对应的浏览器插件并启用 ，具体参考链接[Chrome 扩展](待补充)
(若排除以上情况之后，可具体查看下方“打开浏览器失败”的异常排错思路办法)

</font>
</br></br>
---
</br>

#### 【报错异常】所请求的剪贴板操作失败。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0004.png)
</br>【原因分析】：剪贴板调用和实时的运行环境有关，实现上是和命令行一致的。当剪贴板被占用，或者内存不足时就会失败。

<font color=5a6877>
</br>**【解决办法-AA0004】**：为避免出现这个错误可以管理PC内存，检查剪贴板占用，组件前增加延迟、重试或trycath之后选择失败后继续，或者使用其他组件来实现，比如发送快捷键
</font>
</br></br>
---
</br>


#### 【报错异常】用户回调引发异常
* 请检查异常堆栈和内部异常，以确定失败的回调。回调异常的root cause，或者“使用模拟键盘组件会导致流程随机中断，并且可能会伴随“句柄无效”日志”

<font color=5a6877>
</br>**【解决办法-AA0005】**：淘宝上买 幽灵键鼠 硬件,然后用[模拟键盘合集](https://marketplace.encoo.com/?entry_url=https%3A%2F%2Fwww.encoo.com%2F#/activity/detail?lang=zh-cn&packageId=Automation.KeyboardActivity)里的那个组件 

</font>
</br></br>
---
</br>


#### 【报错异常】句柄无效

<font color=5a6877>
</br>**【解决办法-AA0006】**：同解决办法-AA0005

</font>
</br></br>
---
</br>


#### 【报错异常】云扩录制器奔溃了

![](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0007.jpg)
<font color=5a6877>
【原因分析】：环境权限问题导致，偶发异常
</br>**【解决办法-AA0007】**：管理员权限执行
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0007-1.png)

</font>
</br></br>
---
</br>

#### 【报错异常】不能根据选择器获取窗体

<font color=5a6877>
【原因分析】
可能1、可能iframe的问题，谷歌会将这种弹框拦截，视觉上展示了，但是自动化取不到。
可能2、应该是卡在第一层窗体了
</br>**【解决办法-AA0008】**：
* 第一步、将这个窗口设置成不拦截，后面可以点击到了
* 第二步、若第一步中可能1排查不存在则验证下元素，进一步排查卡在第一层窗体的哪里 

</font>
</br></br>
---
</br>

#### 【报错异常】Bitblt调用失败Error:6

<font color=5a6877>
【原因分析】
- 可能1. 运行时，可能系统进入锁屏状态了
- 可能2. 运行时，窗口最小化就会出现这个问题

</br>**【解决办法-AA0009】**：如果是企业版机器人的话，自带了rdp会话保持功能，如果是远程的话勾选下就好了。

</font>
</br></br>
---
</br>



#### 【报错异常】打开浏览器失败

<font color=5a6877>
</br>**【解决办法-AA0010】**：一般情况下 ，首先请确认是否安装了对应的浏览器插件并启用 ，具体参考链接：[Chrome 扩展]()

</font>
</br></br>
---
</br>

#### 【报错异常】手机自动化，Poco Service服务启动异常
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0011.png)
<font color=5a6877>
</br>**【解决办法-AA0011】**：如果用过旧版本的服务端?在“设置”--“应用”里面找到pocoservice的两个软件、Yosemite、Applistmanager软件都卸载删除，重启服务端，再重新连接，其中pocoservice有两个应用，在设置-应用中找到都删载掉。

</font>
</br></br>
---
</br>


#### 【报错异常】手机自动化，请确保移动设备管理器已打开，已有设备连接
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0012.png)
<font color=5a6877>
</br>**【解决办法-AA0012】**：
1. 确认编辑器菜单栏中”工具 > 移动设备管理器“ 是否已打开。
2. 如果已打开仍未解决，重启移动端服务管理器。

* 移动端服务包无法打开：Failed to execute script EncooAndroidAutomation![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AA0012-1.png)
1. 确认该服务包的版本是否最新，如果非最新，需要重新下载最新版本的服务包。
2. 确认该计算机网络是否正常，如果没有网络则无法获取到网络地址无法打开该应用。

</font>
</br></br>
---
</br>



### 2.5 数据表/数据库自动化

#### 【报错异常】error 0: Authentication to host 'localhost' for user 'root' using method 'caching_sha2_password' failed with message: Reading from the stream has failed.

<font color=5a6877>
</br>**【解决办法-AC0030】**：
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0030.jpg)
</font>
</br></br>
---
</br>

#### 【报错异常】Loading local data is disabled; this must be enabled on both the client and server sides

<font color=5a6877>
</br>**【解决办法-AC0031】**：需要在客户端连接字符串设置 AllowLoadLocalInfile=true;服务端设置 SHOW GLOBAL VARIABLES LIKE 'local_infile';SET GLOBAL local_infile = 'ON';</br>
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0031.png)

</font>
</br></br>
---
</br>

#### 【报错异常】无法加载DLL“db2app.dll”：找不到指定的模块（异常来自HRESULT：0x8007007E）
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0032-1.png)

<font color=5a6877>
</br>**【解决办法-AC0032】**：步骤如下，
1. 确认Db2扩展是否已经安装，若更新过编辑器或者机器人则需要重新安装Db2扩展
2. Db2 数据库访问驱动DLL需要C++运行时，一般新电脑没有C++运行时，安装即可，链接：连接数据库_数据库
3. 若以上步骤还是提示该问题，需要检查Windows 系统版本，是否是Windows Embedded Standard，根据系统是 64 位系统还是 32 系统下载安装。 
●  [点击下载-安装x64：](https://share.weiyun.com/FFxPWka7 )
●  [点击下载-安装x86：](https://share.weiyun.com/DBAnBZBe)

</font>
</br></br>
---
</br>

#### 【报错异常】连接已经是本地事务处理或分布式事务处理的一部分

<font color=5a6877>
</br>**【解决办法-AC0033】**：检查事务组件是否嵌套事务组件

</font>
</br></br>
---
</br>


### 2.6 邮件自动化

#### 【报错异常】获取邮件信息失败

<font color=5a6877>
</br>**【解决办法-AC0034】**：查看是否配置了邮箱的账户信息，如果配置了邮箱名称（不是邮箱地址，见图1），使用邮箱名称填写获取邮件

![-w220](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0034-1.png)![-w300](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0034-2.png)

</font>
</br></br>
---
</br>

#### 【报错异常】发送邮件失败。535: Login Fail. Please enter your authorization code to login.
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0035.png)
<font color=5a6877>
【原因分析】：
- 可能1：账密填写错误，注意此处的密码不是填写登入密码，而是授权码，详见链接：[QQ邮箱授权码如何获取？](https://jingyan.baidu.com/article/ac6a9a5eb439f36b653eacc0.html)
- 可能2：系统规则判定，对同一个账号发送太多邮件，触发了邮件的广告邮件或垃圾邮件机制，限制了发送。

</br>**【解决办法-AC0035】**：
* 方法1：再次确认一下，账号和密码有没填错；
* 方法2：修改用户配置 选现=》信任中心=》信任中心设置=》编程访问，选择从不向我发出警告的选项

</font>
</br></br>
---
</br>

#### 【报错异常】连接服务器失败
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0036.jpg)
<font color=5a6877>
</br>**【解决办法-AC0036】**：查看自己邮箱设置里面的smtp配置（参考163的配置，如图5），通常私有的邮箱服务器会自己配置smtp,pop3等服务，需要联系自己公司邮箱管理员查询相关信息了；
![-w300](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0036-1.png)![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0036-2.png)
</font>
</br></br>
---
</br>


#### 【报错异常】[错误]Outlook的COM端口被占用，请检查是否有插件占用改端口或者关闭Outlook客户端。
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0037.png)
<font color=5a6877>
</br>**【解决办法-AC0037】**：Outlook的配置信息截个图，提示端口被占用（环境问题）客户关闭客户端重启就好）。

</font>
</br></br>
---
</br>


### 2.7 其他异常报错(系统组件、远程、流程执行…)

#### 【报错异常】call remote method timeout,method name : invokeRemoteUiObjectAsync
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0038-1.png)
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0038-2.png)

<font color=5a6877>
</br>**【解决办法-AC0038】**：远程桌面断开后 需要保持RDP会话得，企业版机器人选择里面有保持RDP会话选项。
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0038.png)
</font>
</br></br>
---
</br>

#### 【报错异常】解压缩文件失败。Data descriptor signature not found

<font color=5a6877>
</br>**【解决办法-AC0039】**：下载7-zip，用“执行命令行”组件，进行命令行解压 ，7z命令行(7z.exe -x archive.zip)解压.[下载链接](https://sparanoid.com/lab/7z/)

</font>
</br></br>
---
</br>

#### 【报错异常】请检查是否已安装机器人并处于正常运行状态
![](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0009.jpg)
<font color=5a6877>
【原因分析】：机器人服务未开启
</br>**【解决办法-I0009】**：在任务管理器中，将机器人的服务开启，具体操作图示如下
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0009-1.png)


</font>
</br></br>
---
</br>


#### 【报错异常】服务未正常启动，请尝试手动启动服务或重启电脑

<font color=5a6877>
</br>**【解决办法-I0010】**：同解决办法-I0009

</font>
</br></br>
---
</br>


#### 【报错异常】未检测到服务，可能被其他软件卸载
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0002.png)
<font color=5a6877>
</br>**【解决办法-R0002】**：关闭杀毒软件重装一下

</font>
</br></br>
---
</br>

#### 【报错异常】机器人执行时报错，错误：无法终止进程……原因：拒绝访问
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0003.png)
<font color=5a6877>
【原因分析】：类似拒绝访问的，大多是部署流程的时候 权限配置问题 。
</br>**【解决办法-R0003】**：除了以管理员权限运行机器人外，还需要在执行流程的时候，勾选“以管理员权限执行”。
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0003-1.png)
</font>
</br></br>
---
</br>

#### 【报错异常】[Error] 未能转换部分或所有标识引用
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0004.png)
<font color=5a6877>
【原因分析】：
确认当前登录的windows用户是不是新建出来的 或登录激活的别的windows用户
</br>**【解决办法-R0004】**：如果是的话，注销一下无用的windows session 或者重启一下电脑用正确的用户信息登录。

</font>
</br></br>
---
</br>

#### 【报错异常】活动"Encooworkflow.Main"的CacheMetadata引发了"System.Xaml.XmalObjectWriterException":无法设置未知成员…… 请确认相关的组件是否包含在nuget目录下
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0005.jpeg)
<font color=5a6877>
</br>**【解决办法-R0005】**：首先看下，这个里面的提示的相关组件，属于内置编辑器组件还是市场组件？
- 可能1、是市场组件，说明当前流程运行的编辑器或机器人上缺少这个组件，那就去云扩市场上下载一下
- 可能2、是内置编辑器组件：而且编辑器运行没问题，上传控制台，然后机器人执行就出错，说明这个地方是高版本流程在低版本机器人上运行导致的，需要升级一下机器人
【解决思路】：
可能1、编辑器或者机器人里面点击安装一下 对应市场上面的组件，如果是内网，参考以下文档[离线使用组件市场中的组件](待补充）
可能2、去升级机器人版本至对应的新版本 然后清空下%userprofile%\.nuget\packages再安装
</font>
</br></br>
---
</br>

#### 【报错异常】“HTTPSConnectionPool(host='digpro.ininin.com', port=443): Max retries exceeded with url: /dpsthird/api/v1/production/save_or_update (Caused by NewConnectionError(': Failed to establish a new connection: [Errno 11001] getaddrinfo failed'))”

<font color=5a6877>
【原因分析】：
具体原因参考链接《解决python爬虫requests.exceptions.SSLError: HTTPSConnectionPool(host=‘XXX‘, port=443)问题》https://blog.csdn.net/weixin_44683255/article/details/123706686
</br>**【解决办法-R0006】**：可以在流程设置一个监听，用“try catch”组件，异常了发送邮件或什么预警处理一下

</font>
</br></br>
---
</br>

#### 【报错异常】未能生成XXX视图
![](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0011-1.png)

<font color=5a6877>
</br>**【解决办法-I0011】**：
第一步 ：新建项目，拖一个之前组件缺失的组件
如果报错，清空%UserProfile%\.nuget\packages， 重新打开编辑器，新建项目，如果还报错，找小R

第二步：查看处理项目的project.json文件
做完以后，新建项目可以，但是错误的项目还是有组件缺失，查看项目的project.json,如果project.json里面的settings属性为空，关闭项目，把1里面新建项目的project.json里面的settings复制过来，再打开项目。 如果不为空，清空%UserProfile%\.nuget\packages， 重新打开编辑器，还是报错，找官方技术支持

</font>
</br></br>
---
</br>


#### 【报错异常】此组件缺失，或无法正常加载
![](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0011-2.png)

<font color=5a6877>
</br>**【解决办法-I0012】**：同解决办法解决办法-I0011

</font>
</br></br>
---
</br>


#### 【报错异常】类型XXX的对象无法转换为类型XXX
* 突然打开所有的项目都提示这个，如何处理？

[错误] 类型“System.Action`2[System.Activities.Presentation.Model.ModelItem,BotTimeUI.Common.Mobile.MobileRecordType]”的对象无法转换为类型“System.Action`2[System.Activities.Presentation.Model.ModelItem,BotTimeUI.Common.Mobile.MobileRecordType]”。

<font color=5a6877>
</br>**【解决办法-I0013】**：%userprofile%\.nuget\packages 把这个地址下的文件都删除,然后重装

</font>
</br></br>
---
</br>


#### 【报错异常】[错误] Method not found…
![-w500](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0014-1.png)


<font color=5a6877>
</br>**【解决办法-I0014】**：
* Step1：复制` %UserProfile%\.nuget\packages\automationactivity`路径至资源管理器中，查看该路径下最高版本是多少

* Step2：复制`%UserProfile%\AppData\Local\EncooStudio\{version}\buildinActivities`路径至资源管理器中，查看该路径下的`automationactivity`版本号是多少


* Step3：如果【Step1】和【Step2】中的版本号不一致，说明本地有高版本的依赖项，此时可以
    * 方法一：升级编辑器和机器人到最新版本（推荐）
    * 方法二：升级到【Step1】的编辑器的版本，需要知道【Step1】里面的automationactivity的版本对应的编辑器的版本
* Step4：关闭编辑器，清空`%UserProfile%\.nuget\packages`，重新打开编辑器，新建一个项目，关闭这个项目，断网，打开报错的项目

</font>
</br></br>
---
</br>


#### 【报错异常】[错误] Main.xaml: “对类型“……”的构造函数执行符合指定的绑定约束的调用时引发了异常。”，行号为“XXX”，行位置为“XXX”。 行：XXX, 列：XX

<font color=5a6877>
</br>**【解决办法-I0015】**：同解决办法-I0014

</font>
</br></br>
---
</br>


#### 【报错异常】活动“登录”的CacheMeta 引发了"System.Xaml.……:无法创建未知类型"{XXX}……"。请确认相关的组件包是否包含在nuget目录下"
![-w800](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0016.png)
<font color=5a6877>
</br>**【解决办法-I0016】**：导入的流程在导出时需要选择包含对应的依赖项

</font>
</br></br>
---
</br>

