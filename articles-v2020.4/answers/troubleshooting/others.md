# Error6：其他报错


#### Q：执行JavaScript代码组件失败。详细错误信息：调用JavaScript业务函数返回失败：test_demo is not define 

<br>

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633117867946.jpg"/>

<font color=5a6877>
<br><br>

**【解决办法-AC0052】**: 如下所示 ，字符串类型的值要双引号转义

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633118022222.jpg"/>

</font>
<br><br>
---
<br> 

#### Q：机器人导入dgs报错 “Database was not shutdown cleanly. Revocery must first be run to properly compelete database operations for the previous shutdown ”

<br>


 <img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633073662017.jpg"/>
 
<font color=5a6877>
<br><br>

**【解决办法-R0009】**: 尝试将data（%localappdata%\encoo\encoo robot\data 删除前提醒备份）文件删除，再重新导入。

</font>
<br><br>
---
<br> 

#### Q：点击选择器会弹窗未响应，弹窗提示“Encoo Studio 未响应”，点击选择器会弹窗未响应，等待卡顿好几秒，每次都出现。

<br>

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16632954820060.jpg"/>

<font color=5a6877>
<br><br>

**【解决办法-R0008】**:

有几种可能
1、杀毒软件没关
2、 net framework有问题，缺少一些库，重新安装一下.net framework


<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16632955890051.jpg"/>

</font>
<br><br>
---
<br> 

#### Q：[错误]在"System.Windows.StaticResourceExtension"上提供值时引发了异常。导入dgs的时候出现的报错.且流程包导入导出的版本都一致。
* 导出dgs的编辑器版本：2206.14 
* 导入dgs的编辑器版本：2206.14 

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0007_1.jpg"/>

<br>

<font color=5a6877>
<br>

**【解决办法-R0007】**:
先查看当前环境用的是哪个.net版本
编辑器安装目录下有对应.net版本的中文语言包，找到并安装

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0007_2.png"/>


</font>
<br><br>
---
<br> 

<br>

#### Q：[错误]循环操作失败，详细信息：Specified cast is not valid.

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0044.png"/>


<font color=5a6877>
<br><br>

**【解决办法-AC0044】** ：把循环的参数重新填一下。把foreach组件那里使用这个变量的那个属性，删掉，然后鼠标移出来，让它失去焦点，然后再移进去重新输入下

</font>
<br><br>
---
<br>


#### Q：call remote method timeout,method name : invokeRemoteUiObjectAsync

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0038-1.png"/>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0038-2.png"/>

<font color=5a6877>
<br><br>

**【解决办法-AC0038】** ：远程桌面断开后 需要保持RDP会话得，企业版机器人选择里面有保持RDP会话选项。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0038.png"/>


</font>
<br><br>
---
<br>

#### Q：解压缩文件失败。Data descriptor signature not found

<font color=5a6877>
<br>

**【解决办法-AC0039】** ：下载7-zip，用“执行命令行”组件，进行命令行解压 ，7z命令行(7z.exe -x archive.zip)解压.[下载链接](https://sparanoid.com/lab/7z/)

</font>
<br><br>
---
<br>

#### Q: 编辑器发布到机器人失败，错误原因：Database corrupted

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0017.png"/>

<br>

<font color=5a6877>
<br> 

**【解决办法-I0017】** ：重新下载机器人后 ，重装机器人

</font>
<br><br>
---
<br> 


#### Q：请检查是否已安装机器人并处于正常运行状态

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0009.jpg"/>

<br>

<font color=5a6877>

【原因分析】：机器人服务未开启

<br> 

**【解决办法-I0020】** ：在任务管理器中，将机器人的服务开启，具体操作图示如下

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0009-1.png"/>

</font>
<br><br>
---
<br>


#### Q：服务未正常启动，请尝试手动启动服务或重启电脑

<font color=5a6877>
<br> 

**【解决办法-I0010】** ：同解决办法-I0009

</font>
<br><br>
---
<br>


#### Q：未检测到服务，可能被其他软件卸载

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0002.png"/>

<font color=5a6877>
<br> 

**【解决办法-R0002】** ：关闭杀毒软件重装一下

</font>
<br><br>
---
<br>

#### Q：机器人执行时报错，错误：无法终止进程……原因：拒绝访问

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0003.png"/>

<br>
<font color=5a6877>
【原因分析】：类似拒绝访问的，大多是部署流程的时候 权限配置问题 。

<br>

**【解决办法-R0003】** ：除了以管理员权限运行机器人外，还需要在执行流程的时候，勾选“以管理员权限执行”。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0003-1.png"/>

</font>
<br><br>
---
<br>

#### Q：[Error] 未能转换部分或所有标识引用

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0004.png"/>
<br>
<font color=5a6877>

【原因分析】：
确认当前登录的windows用户是不是新建出来的 或登录激活的别的windows用户

<br>

【解决办法-R0004】 ：如果是的话，注销一下无用的windows session 或者重启一下电脑用正确的用户信息登录。

</font>
<br><br>
---
<br>

#### Q：活动"Encooworkflow.Main"的CacheMetadata引发了"System.Xaml.XmalObjectWriterException":无法设置未知成员…… 请确认相关的组件是否包含在nuget目录下

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/R0005.jpeg"/>

<font color=5a6877>
<br>
<br>

**【解决办法-R0005】** ：首先看下，这个里面的提示的相关组件，属于内置编辑器组件还是市场组件？
- 可能1、是市场组件，说明当前流程运行的编辑器或机器人上缺少这个组件，那就去云扩市场上下载一下
- 可能2、是内置编辑器组件：而且编辑器运行没问题，上传控制台，然后机器人执行就出错，说明这个地方是高版本流程在低版本机器人上运行导致的，需要升级一下机器人

<br>

【解决思路】：
可能1、编辑器或者机器人里面点击安装一下 对应市场上面的组件，如果是内网，参考以下文档[离线使用组件市场中的组件](https://academy.encoo.com/zh-cn/wiki/BestPractices/offline-use-activitymarket.md)
可能2、去升级机器人版本至对应的新版本 然后清空下`%userprofile%\.nuget\packages`再安装

</font>
<br><br>
---
<br>

#### Q：“HTTPSConnectionPool(host='digpro.ininin.com', port=443): Max retries exceeded with url: /dpsthird/api/v1/production/save_or_update (Caused by NewConnectionError(': Failed to establish a new connection: [Errno 11001] getaddrinfo failed'))”

<br>
<font color=5a6877>
【原因分析】：
具体原因参考链接《解决python爬虫requests.exceptions.SSLError: HTTPSConnectionPool(host=‘XXX‘, port=443)问题》https://blog.csdn.net/weixin_44683255/article/details/123706686
<br>

**【解决办法-R0006】** ：可以在流程设置一个监听，用“try catch”组件，异常了发送邮件或什么预警处理一下

</font>
<br><br>
---
<br>

#### Q：未能生成XXX视图

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0011-1.png"/>


<font color=5a6877>
<br>

**【解决办法-I0011】** ：

* 第一步 ：新建项目，拖一个之前组件缺失的组件

    如果报错，清空`%UserProfile%\.nuget\packages`， 重新打开编辑器，新建项目，如果还报错，找小R

* 第二步：查看处理项目的project.json文件

    做完以后，新建项目可以，但是错误的项目还是有组件缺失，查看项目的project.json,如果project.json里面的settings属性为空，关闭项目，把1里面新建项目的project.json里面的settings复制过来，再打开项目。 如果不为空，清空`%UserProfile%\.nuget\packages`， 重新打开编辑器，还是报错，找官方技术支持

</font>
<br><br>
---
<br>


#### Q：此组件缺失，或无法正常加载

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0011-2.png"/>

<font color=5a6877>
<br>

**【解决办法-I0012】** ：同解决办法解决办法-I0011

</font>
<br><br>
---
<br>


#### Q：类型XXX的对象无法转换为类型XXX

突然打开所有的项目都提示这个，如何处理？[错误] 类型“System……”的对象无法转换为类型……”。

<font color=5a6877>
<br> 

**【解决办法-I0013】** ：`%userprofile%\.nuget\packages` 把这个地址下的文件都删除,然后重装

</font>
<br><br>
---
<br>


#### Q：[错误] Method not found…

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0014-1.png"/>


<font color=5a6877>
<br> 

**【解决办法-I0014】** ：
* Step1：复制` %UserProfile%\.nuget\packages\automationactivity`路径至资源管理器中，查看该路径下最高版本是多少

* Step2：复制`%UserProfile%\AppData\Local\EncooStudio\{version}\buildinActivities`路径至资源管理器中，查看该路径下的`automationactivity`版本号是多少


* Step3：如果【Step1】和【Step2】中的版本号不一致，说明本地有高版本的依赖项，此时可以
    * 方法一：升级编辑器和机器人到最新版本（推荐）
    * 方法二：升级到【Step1】的编辑器的版本，需要知道【Step1】里面的automationactivity的版本对应的编辑器的版本
* Step4：关闭编辑器，清空`%UserProfile%\.nuget\packages`，重新打开编辑器，新建一个项目，关闭这个项目，断网，打开报错的项目

</font>
<br><br>
---
<br>


#### Q：[错误] Main.xaml: “对类型“……”的构造函数执行符合指定的绑定约束的调用时引发了异常。”，行号为“XXX”，行位置为“XXX”。 行：XXX, 列：XX

<font color=5a6877>
<br> 

**【解决办法-I0015】** ：同解决办法-I0014

</font>
<br><br>
---
<br>


#### Q：活动“登录”的CacheMeta 引发了"System.Xaml.……:无法创建未知类型"{XXX}……"。请确认相关的组件包是否包含在nuget目录下"

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/I0016.png"/>

<font color=5a6877>
<br> 

**【解决办法-I0016】** ：导入的流程在导出时需要选择包含对应的依赖项

</font>
<br><br>
---
<br>

#### Q："执行Python代码报错GBK错误：“UnicodeEncodeError:'gbk' codec can't encode character '\xa5' in position 0:illegal multibyte sequence” "

![error1](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/error06-00001.png)

**【解决办法-I0017】** 主要原因是python自身编码与Windows控制台编码不一致。需要python做编码处理才行。

**第一种方法:** 直接替换出错的内容

```
import requests 
url = 'https://blog.csdn.net/jianhong1990/article/details/17349537'
print(requests.get(url).text.replace('\xa0', ' '))
```

**第二种方法:** 再解码

先用 GBK 编码，加个 ignore 丢弃错误的字符，然后再解码。

```
import requests
url = 'https://blog.csdn.net/jianhong1990/article/details/17349537'
print(requests.get(url).text.encode('gbk', 'ignore').decode('gbk')
```


**第三种方法:** 修改控制台编码

新建一个 cmd.reg, 输入代码：

```
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Console\%SystemRoot%_system32_cmd.exe]
"CodePage"=dword:0000fde9
"FontFamily"=dword:00000036
"FontWeight"=dword:00000190
"FaceName"="Consolas"
"ScreenBufferSize"=dword:232900d2
"WindowSize"=dword:002b00d2
```

保存后运行。如果 Ctrl+B 无效，用 python.exe 打开.py程序后再试一次。

> 解决办法转自：https://www.jb51.net/article/143722.htm

</font>
<br><br>
---
<br>


#### Q：更新机器人客户端为最新版后有两个流程出现异常，编辑器和旧版机器人运行都没问题，有解决方案吗?


<font color=5a6877>
<br> 

**【解决办法-I0018】** ：打开文件资源管理器，进入 ```C:\Users\UserName``` 下，删除“```.nuget```”文件夹，之后重启机器人

![error1](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202005240001.png)


</font>
<br><br>
---
<br>

#### Q：配置python环境报错，“xxxx.exe不是有效的python环境路径”，但本地py是有这个exe


<font color=5a6877>
<br> 

![error1](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202006020001.png)


**【解决办法-I0019】** ：把lib目录复制到Scripts里面去，让python.exe和lib在同一层目录。


</font>
<br><br>
---
<br>