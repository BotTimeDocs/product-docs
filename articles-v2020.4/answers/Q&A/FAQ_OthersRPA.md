# FAQ4：其它_流程开发问题

<br>

<br>

#### Q：编辑器卡顿，偶尔报错：out of memory

<br>

<font color=5a6877>
<br><br>

**【解决办法-A5_00031】**: 多数情况下是由于当前流程过于复杂，组件嵌套太多。 建议将复杂流程拆分成多个子流程，并使用[调用子流程](../../Activities/WorkflowControl/InvokeWorkflow.md)组件串联流程逻辑。


</font>
<br>

#### Q：机器人上是管理员启动的，如何让流程在控制台定时启动时候也管理员身份运行？

<br>

<font color=5a6877>
<br><br>

**【解决办法-A5_00030】**:编辑器右键“项目”，然后点项目设置-常规-执行权限，可以选择“以管理员权限执行”。另外机器人客户端单独执行一个流程的时候 可以勾选 

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633121945762.jpg"/>


</font>
<br><br>
---
<br> 

#### Q：使用outlook出现弹窗“有一个程序正试图访问储存在Outlook中的电子邮件地址信息……”，这种情况改怎么处理？

<br>

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633120247825.jpg"/>

<font color=5a6877>
<br><br>

**【解决办法-A5_00029】**:管理员启动，然后按下图设置一下。outlook有个机制，一个月后应该还会出现，因为一个月后它会自动开启防护，到时候再同样设置一下

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633120598818.jpg"/>

</font>
<br><br>
---
<br> 

#### Q：获取邮件时需要获取到名称才能判断该文件是否存在，该如何获取附件名称？

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633119283860.jpg"/>

<br>


<font color=5a6877>
<br><br>

**【解决办法-A5_00028】**: 如图所示

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633119364546.jpg"/>

</font>
<br><br>
---

<br> 

#### Q：运行流程时，对于一些不定时出现的弹框，怎么解决？

<br>


<font color=5a6877>
<br><br>

**【解决办法-A5_00027】**: 思路是使用组件“等待元素出现”，结合“trycatc”组件。发现了就关闭，没有就正常执行

</font>
<br><br>
---
<br> 


#### Q：获取结构化数据选择器下一页是否支持变量？

<br>


<font color=5a6877>
<br><br>

**【解决办法-A5_00026】**: 目前获取结构化数据的下一页，暂不支持变量

</font>
<br><br>
---
<br> 


#### Q：RPA流程中Excel如何实现自适应列宽？

<br>

<font color=5a6877>
<br><br>

**【解决办法-A5_00024】** :需要写C#代码，点击查看[具体参考链接](https://stackoverflow.com/questions/2884356/how-do-i-auto-size-columns-through-the-excel-interop-objects)


 <img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633095322605.jpg"/>
 
</font>
<br><br>
---
<br> 

#### Q：1.1.2204.10升级1.1.2206.14 出现插件扩展报错。升级到版本后有插件扩展报错的问题，退到10版本又好了，为什么会这样？


<br>

<font color=5a6877>
<br><br>

**【解决办法-A5_00023】**:

可能存在以下原因，导致了如上的问题。安装的谷歌浏览器(32位）跟系统位数（64位）不匹配，导致出现插件异常，安装64位的谷歌浏览器就没问题了

</font>
<br><br>
---
<br> 

 
#### Q：老版本流程发布的时候市场显示为空
 
 
 <img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16632974314156.jpg"/>
 
 <br>

<font color=5a6877>
<br><br>

**【解决办法-A5_00022】**: 检查下本地管理市场有没有可用的组件市场


 <img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16632974500283.jpg"/>
 
</font>
<br><br>
---
<br> 


#### Q：手机自动化，poco一直显示连接中，如何处理？

<br>


<font color=5a6877>
<br><br>

**【解决办法-A5_00021】**:

卸载完再重新连接。手机的“设置”-“应用和服务”-“应用管理”里面找到pocoservice的两个应用卸载删除掉，Applistmanager、Yosemite也卸载删除掉。一个叫“PocoService”，一个叫“com...pocoservice....”类似的都卸载掉

</font>
<br><br>
---
<br> 

#### Q：使用机器人打开网页登录会经常白屏，打不开网页。但是手动复制网址打开就正常的，会是什么原因？

<br> 


<font color=5a6877>
<br><br>

**【解决办法-A5_00020】** : 试下先打开一个其他网页如“百度”，然后用当前页跳转跳转过去

</font>
<br><br>
---
<br> 

#### Q：qq截图手动执行好的定时任务触发截图不全，怎么办？

<br>


<font color=5a6877>
<br><br>

**【解决办法-A5_00019】**: 大可能是分辨率问题，调整一下电脑显示器的分辨率即可。

</font>
<br><br>
---
<br> 

<br>

#### Q：远程时复制组件的时候界面会卡住动不了，过一会才会正常是为什么？

<br>


<font color=5a6877>
<br><br>

**【解决办法-A5_00018】**: 向日葵的剪切板关掉就不卡了

</font>
<br><br>
---
<br> 

#### Q：验证sap sap有的地方识别不到怎么办？SAP是普通权限，编辑器用管理员权限启动的

<br>



<font color=5a6877>
<br><br>

**【解决办法-A5_00017】**:

确认好配置对应[SAP自动化配置步骤_rz11权限](https://academy.encoo.com/wiki/Activities/SAP/SAP%20Configuration.md?uuid=087d07a5-2a4d-5d5b-9622-53fefb2f74e7)并确认编辑器权限要跟SAP保持一致

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/08/29/16617462104801.jpg"/>


    
</font>
<br><br>
---
<br> 
 
<br>

#### Q：独立桌面情况下如何打开扩展[报错]：打开浏览器失败。不用独立桌面的时候是成功的

<br>

 <img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A5_00016.png"/>

<font color=5a6877>
<br><br>

**【解决办法A5_00016】**: 

同样需要在远程的浏览器中”扩展程序“中安装启用一下插件

</font>
<br><br>
---
<br> 

#### Q：RPA有ssh组件吗？

<br>


<font color=5a6877>
<br><br>

**【解决办法A5_00015】**: 

试一下 市场的运维组件 

 <img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A5_00015.png"/>

</font>
<br><br>
---
<br> 

#### Q：写入文件组件，换行符如何写入 ？

<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A5_00014.jpg"/>

<font color=5a6877>
<br><br>

**【解决办法A5_00014】**:

`"Start"+'\n'+"End"`   

或者 

`  "Start"+System.Environment.NewLine+"End"`

两种都可以
    
</font>
<br><br>
---
<br> 
 

<br>

#### Q：赋值，double计算结果小数点后面很多位，如何只保留2位 

<br>
<font color=5a6877>
<br><br>

**【解决办法-A5_00013】**: 

以下方示例 ： `c2 = double.Parse(c1.ToString("0.00"));`
    
<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A5_00012.png"/>

</font>
<br><br>
---
<br> 



#### Q：执行C#代码把行赋值后导入克隆表，为什么预览克隆表是空的？kl是克隆的表，我对行赋值后，将这一行导入的克隆表，不是把克隆表直接导入

<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A5_00012.png"/>

<font color=5a6877>
<br><br>

**【解决办法-A5_00012】**:克隆表只复制结构，不复制内容。要用复制表才行
    
</font>
<br><br>
---
<br> 


#### Q：一个子流程中创建的变量如何在其他流程中调用？

<br>

<font color=5a6877>
<br>

**【解决办法-A5_00010】**:

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A5_00010.png"/>


子流程中不用定义变量直接设置参数 ，然后把它改成输出，就可以在外部主流程调用或者子流程。再调用的时候去接受这个子流程传出来的值。

如果是想要把外部变量，在子流程中调用就写输入；
如果是想要外部变量输入进去，再里面更新又反馈出来，就改成输入/输出。

跟 python的class继承类似，具体查看文档[《使用参数》](https://academy.encoo.com/zh-cn/wiki/Studio/process/developProject/Arguments/UseArguments.md?uuid=a5e38ade-2d9a-4409-babb-46fa26fd86aa)

</font>
<br><br>
---
<br> 


#### Q：DateTIme.now 拿到当前时间之后怎么输出格式化文本 比如“yyyy/MM/dd”“MM/dd hh:mm:ss”这样？

<br>

<font color=5a6877>
<br>

**【解决办法-A5_00011】**：

//格式化日期为“年年年年-月月-日日”： DateTime.Now.ToString("yyyy-MM-dd"); //格式化日期为“年年年年-月月-日日 时时:分分:秒秒”： DateTime.Now.ToString("yyyy-MM-dd HH:mm:ss");

编辑器都是用C# 做的，之后有这种格式问题都可以用C# 去做，可以参考这个连接。更多日期数据格式类型 参考链接：
https://blog.csdn.net/banzhenfei/article/details/114010195?ops_request_misc=%257B%2522r+scm%2522%253A%252220140713.130102334..%2522%257D&request_id=165837215716781432938224&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-114010195-null-null.142^v33^experiment_28w_v1,185^v2^control&utm_term=C%23%20%E6%97%B6%E9%97%B4&spm=1018.2226.3001.4187

</font>
<br><br>
---
<br> 

#### Q：2022年7月 新版本发布后 为什么没有引用项目 这个选项？

 <br>

<font color=5a6877> 【解决办法A5_00001】: 

至2022年7月 新版本发布
7月新版本编辑器，合并了组件项目及前期引用项目的用法，通过创建一个组件项目，并将其发布到组件市场，在其他项目中进行使用(而不是仅限于单个项目引用) ，具体详见文档：[《创建组件项目》](https://academy.encoo.com/zh-cn/wiki/Studio/process/CreateProject/CreateLibrary.md?uuid=4f2d5853-ffb5-45e0-85e2-4decc0dd15d7)


如何将流程发布成组件 可以看文档：[《如何将流程发布成组件》](https://academy.encoo.com/zh-cn/wiki/BestPractices/workflow-activity.md?_v=v2020.4&uuid=1b1ab067-7487-4efe-b35a-5dfdc6638847)

2022年7月之后的版本 界面上目前不支持，已开发的流程 若想要引用，具体操作步骤可见文档：[《【技术方案】(旧版本创建好的流程项目) "引用项目"在 2206.10之后的编辑器使用》](https://c9vrjkv7og.feishu.cn/docx/doxcnd7y9aDxQNC9RI2Uzxj78Wg)


 </font><br><br>
 ---
 <br>

#### Q：屏幕解锁，设置了对应的解锁组件，但是不生效 ？

<br>

<font color=5a6877> 【解决办法A5_00002】: 

* 排查方法一：尝试通过组件进行锁屏，即在流程中配对使用锁屏与解锁组件。目前已知在个别特殊环境下，手动锁屏时解锁组件无法正常解锁，但通过组件锁屏时能够正常解锁。

* 排查方法二：在“控制面板 > 系统与安全 > 管理工具 > 本地策略”下找到“交互式登录：无需按 Ctrl+Alt+Del”这一项，勾选“已启用”项。

 </font><br><br>
 ---
 <br>


#### Q：市场组件如何重命名？
<br>

<font color=5a6877>
<br>**【解决办法-A5_00003】**：可以双击更改

</font>
<br><br>
---
<br> 

#### Q：如何设置编辑器成英文版本
<br>

<font color=5a6877>
<br>**【解决办法-A5_00004】**：切换成英语版本：
`%userprofile%\AppData\Local\Encoo Studio\app-1.1.2111.6`（编辑器安装目录）
下的Encoo.Studio.exe.Config
zh-CN 改成 en-US

</font>
<br><br>
---
<br> 


#### Q：查询sql，查询语句如何传参？
请问数据库连接操作里，union的查询sql应该怎么配置？查询条件要外面传入的。我看查询语句组件好像不支持传参。
可以参数写成{0}，然后跟在sql后面写参数变量吗

<br>

<font color=5a6877>
<br>

【解决办法-A5_00009】：支持填写参数/变量的 ，以拼接的方式实现

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A_500009.png"/>


</font>
<br><br>
---
<br> 

#### Q：exe文件放在项目路径下，执行命令行的命令该怎么写？


<br>

<font color=5a6877>
<br>

【解决办法-A5_00010】：可以直接运行当前项目文件的exe文件（相对路径）


<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202005230001.png"/>

或定义个变量使用 
```Environment.GetEnvironmentVariable("CurrentProjectSourcePath", EnvironmentVariableTarget.Process) ``` 
获取当前项目路径，然后再在组件中拼接：

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202005230002.png"/>

</font>
<br><br>
---
<br> 