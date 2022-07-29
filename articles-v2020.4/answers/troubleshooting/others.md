

### 一、其他(报错索引)

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



<br><br><br>

###  二、具体解决办法

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

</br>
**【解决办法-R0003】**：除了以管理员权限运行机器人外，还需要在执行流程的时候，勾选“以管理员权限执行”。

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

</br>

【解决办法-R0004】 ：如果是的话，注销一下无用的windows session 或者重启一下电脑用正确的用户信息登录。

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
可能1、编辑器或者机器人里面点击安装一下 对应市场上面的组件，如果是内网，参考以下文档[离线使用组件市场中的组件](https://academy.bottime.com/wiki/BestPractices/offline-use-activitymarket.md?uuid=e6870ddb-2bee-427e-bf93-7f39c0288080）
可能2、去升级机器人版本至对应的新版本 然后清空下`%userprofile%\.nuget\packages`再安装
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
如果报错，清空`%UserProfile%\.nuget\packages`， 重新打开编辑器，新建项目，如果还报错，找小R

第二步：查看处理项目的project.json文件
做完以后，新建项目可以，但是错误的项目还是有组件缺失，查看项目的project.json,如果project.json里面的settings属性为空，关闭项目，把1里面新建项目的project.json里面的settings复制过来，再打开项目。 如果不为空，清空`%UserProfile%\.nuget\packages`， 重新打开编辑器，还是报错，找官方技术支持

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
</br>**【解决办法-I0013】**：`%userprofile%\.nuget\packages` 把这个地址下的文件都删除,然后重装

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

