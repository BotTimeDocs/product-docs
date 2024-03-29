# 管理1、《流程运行概述》

<br>

>导读: 
> 
> * 重在带大家了解
> * 什么是机器人？机器人安装后的程序结构主要是什么？机器人执行多个任务的方式是什么？
> 
>  * 机器人部署类型
>
>   * 流程运行环境:离线环境(无网络)、独立桌面、锁屏/解锁、静默运行
>
>   * 流程运行监控：关于机器人3种监控方式的介绍以及日志详解、录屏、截图

<br><br>

当我们编辑完流程以后，就要开始运行流程。机器人是专门用来运行流程的，比起编辑器，他可以完成一些更复杂，无人值守的业务场景自动化。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-wanglei-product.png"/>



## 一、机器人篇

### 1.1 什么是机器人？

<font color =green>机器人，是自动化流程的执行者，用于执行编辑器生成的自动化流程。</font> 

* 使用机器人可以任意地执行自动化流程，还可以定时地、在无人值守条件下执行流程以满足稍有规模的业务流程。

* 并且在与控制台结合下，可以覆盖大规模的、多机器人协作的业务场景。

<br><br>

机器人是“流程执行者”。它包含以下几层含义:

+ （1）基础使用：一个流程包在通过编辑器进行发布后，机器人就可以执行这个流程包，此时可以完成一些最基础的、需要手动触发的业务场景自动化。

+ （2）进阶使用：结合机器人自身提供的功能，来独立完成一些较复杂的、基础无人值守的业务场景自动化。比如[定时任务](https://academy.encoo.com/zh-cn/wiki/Reference/Robot/CronJob.md)，可以定时的去执行流程。

+ （2）高阶使用：通过配合控制台来完成一些非常复杂的、多机器人配合、无人值守的业务场景，尤其是一些跨环境的、工作量大的场景。

<br><br>

### 1.2 机器人安装后的程序结构主要是什么？


机器人安装完以后会产生一个Windows服务和一个桌面应用程序

* （1）一个名为 Encoo Robot Service 的 Windows 服务程序  
  1. 是机器人的核心程序，负责处理机器人的逻辑 </br>
  2. 一个计算机只存在最多一个该进程 </br>
 </br>

  <img width = '600'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/12/22/16717028484764.jpg"/>
  
 </br>
 </br>

* （2）另一个名为 Robot.exe 的 Windows 桌面应用程序
  1. 是与用户交互的界面程序 </br>
  2. 计算机中的每个用户都可以启动一个进程，不会互相影响 </br>
  
   </br>

  <img width = '100'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/12/22/16717151301963.jpg"/>
  

  </br>
</br>


### 1.3 机器人执行多个任务的方式是什么？

</br>

**（1）任务指定到多个机器人**

创建流程部署，可以指定到多个机器人来执行，调度时候，可以根据指定的机器人列表寻找一个可用机器人来执行自动化流程；
指定多个机器人执行，当执行资源被占用时，可灵活设置以下调度策略：
* 等待可用资源ready后执行；
* 放弃本次调度

</br></br>

**（2）任务指定到机器人组**

创建流程部署，可以指定到一个机器人组，调度时候，可以根据指定的机器人组中寻找一个可用机器人来执行自动化流程；
指定一个机器人组，当所有执行资源被占用时，可灵活设置以下调度策略：
* 等待可用资源ready后执行；
* 放弃本次调度

</br></br></br>

## 二、机器人部署类型

机器人可以部署在服务器或者本地电脑PC/laptop上。
* 一般部署在服务器上是为了做一些进阶使用和高阶使用；
* 而部署在本地电脑PC/laptop上可以做一些基础使用。

</br></br>

不同部署方式：服务器方式部署 VS PC/laptop方式部署

  <img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-DeploymentType.png"/>
  

</br></br>

机器人可以连接公有云的控制台，也可以连接私有化部署的控制台。关于公有云控制台和私有化部署的控制台，可以参看[企业级运维](https://dev-academy.bottime.com/zh-cn/wiki/RunManager/EnterpriseOM.md)。

机器人与控制台通信支持WebSocket与Http协议， 默认使用WebSocket协议。 

> **注意：** Http协议对于实时性和稳定性相对较差，一般用于以下场景：
> * 机器人安装在Windows 8/Windows Server 2016以下的操作系统（不包含win8和winserver2016）
> * 客户环境无法支持WebSocket

</br></br>

## 三、流程运行环境

</br>

### 环境1：离线环境(无网络)
当机器人处于无网或者内网状态无法连接到控制台的时候，我们可以通过本地激活来激活机器人。

</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-activate.png"/>


  
本地激活通过唯一的机器码来获取许可证，激活以后进入机器人用户操作界面，与控制台的连接是断开的。

这种激活方式下，除了控制台的流程以及一些设置不可见（如自动解锁屏幕和RDP远程）之外，机器人其他的功能都能正常使用。


</br></br>

### 环境2：独立桌面

流程在执行前，勾选独立桌面，流程就可以在独立桌面中运行。关于独立桌面介绍可见文档[《如何让流程在独立桌面中运行?》](https://academy.encoo.com/wiki/BestPractices/RunAlone.md)

</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-Independentdesktop.png"/>



</br></br>独立桌面模式会有当前的Windows登录账号打开一个小的桌面，流程将会在这个小的桌面中执行，在独立桌面中的流程不会干扰到正常的桌面，这就意味着用户可以在流程运行的过程中在计算机上继续做其他事情。</br></br>

> **注意：** 
> 独立桌面和正常桌面共享一个Chrome Session, 这代表了独立桌面模式下，在独立桌面与正常桌面中只能打开一个chrome的实例。
> 

</br></br></br>

### 环境3：锁屏/解锁

</br>不管是服务器还是本地电脑PC/laptop, 当计算机不去操作一段时间，都会自动进入锁屏状态。通常我们建议在计算机中将锁屏选项关闭以保证流程的正常运行。</br>

</br>但是在有些场景上，做这种设置是不安全的。机器人为我们提供了一种自动解锁的运行机制。</br></br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-lockscreen.png"/>


</br></br>当机器人开始执行流程的时候，计算机处于锁屏状态，勾选自动解锁功能以后，机器人会使用设置好的用户名和密码解锁计算机，使得流程可以正常的执行。</br></br></br>

### 环境4：静默运行

</br>当流程中界面操作的部分只有浏览器的时候，可以开启静默运行， 即在流程运行时后台打开独立浏览器且不可视，即使用户手动操作浏览器也互不干扰。实现机器人和人同时操作。</br>

</br>在打开浏览器组件的属性里，当打开方式勾选“Selenium”，同时勾选“静默运行”选项，即可静默运行。具体可以参照[打开浏览器组件](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/Browser/OpenBrowser.md)</br>

</br></br>


## 四、流程运行监控

### 4.1 机器人3种监控方式介绍
</br>流程运行过程中有时可能会发生预料之外的异常，此时就需要回顾流程的整个执行过程，以此来检查出现异常的环节以及异常原因。机器人目前提供了以下三种监控方式：</br></br></br>

**方式(1)、日志**

日志是流程执行的默认功能，在每次流程执行时，都会根据流程的实际情况产生对应的日志。 </br></br></br>

**方式(2)、实时日志**

在机器人执行流程时，左侧列表会出现“执行日志”页面的按钮，跳转后的页面会展示当前机器人正在执行的步骤以及实时产生的日志信息。</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-Realtimelog.png"/>


</br></br></br>

**方式(3)、历史日志**

除了在窗口实时展示以外，流程产生的日志也会记录到相应的日志文件中。在“执行记录”页面可以看到每条执行记录都有对应的日志按钮：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-historylog.png"/>


点击“日志”，就可以直接进入目录并查看日志文件。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-journalfile.png"/>

 
### 4.2 日志详解

一条日志除了日志的正文外，还包含了 **日志类型** 与 **日志级别** 两类信息。

</br></br>

**（1）日志类型**

* 系统日志
  * 由机器人自身产生的日志，并且与流程内的逻辑无关，任何流程都会产生该类日志。如：“正在加载流程”、“组件开始：赋值”、“组件错误：未找到指定元素”等等。</br>
  * 这类日志会存放在.log文件中</br>

</br>

* 业务日志
  * 由用户通过“写入日志”组件产生的日志，日志内容没有限制，完全由编写流程的人根据需要使用。</br>
  * 这类日志会存放在*-businesslog.log中</br>

</br></br>

**（2）日志级别**

* **Debug**
  1. 调试日志</br>
  2. 一般用于流程开发者辅助开发或调试错误</br>
  3. 用来记录细致的流程执行信息，如执行步骤。或是将一些变量的值打印出来用于调试流程。</br>
* **Info**
  1. 重要日志</br>
  2. 一般用于流程使用者</br>
  3. 用来记录需要呈现给流程使用者的一些粗略但关键的信息。</br>
* **Error**
  1. 错误日志</br>
  2. 在流程出现异常情况时，用于记录当下的异常信息</br>
  3. 错误日志出现时，机器人会相应地抓取当前计算机画面存放于日志目录中，供用户进行错误分析</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-errorlog.png"/>
 

建议的默认日志级别是**Info级别**，即仅展示关键信息。

而在流程出现难以定位的问题时，将日志级别设置为Debug，根据更细致的日志来定位异常的原因。

</br>
</br>

### 4.3 录屏

如果日志不足以分析问题时，除了进一步完善日志外，也可以使用录屏的方式，将整个流程的执行过程完整录制下来用来定位问题。

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-screenrecording.png"/>


 
</br>
在执行窗口中，勾选了录制视频后，机器人就会将本次的执行过程完整录制下来，并存放于日志目录。</br>
</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-Logdirectory.png"/>


  

</br>

如果为了节省硬盘空间，可以指定仅在流程执行成功或执行失败，才保存录屏文件，否则录屏文件会在流程结束后删除。</br>
</br>
</br>


### 4.4 截图

如果因为计算机性能不足、或是硬盘空间有限等原因无法使用录屏功能时，也可以使用消耗资源更低的执行过程截图功能。</br>
</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-screenshot.png"/>


 
</br>
</br>
执行过程截图会根据流程组件的实际情况，仅在组件与组件之间进行截图，如果单个组件执行时间很长，也只会产生一张截图。</br>
</br>


勾选了执行过程截图的情况下，在流程执行结束后，日志目录会多出一个Screenshots文件夹，用于存放截图。</br>
</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0615-screenshotsave.png"/>
