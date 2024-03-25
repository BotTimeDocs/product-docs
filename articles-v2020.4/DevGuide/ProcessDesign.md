# 指南四《流程设计指南》

<br>

>导读: 
> 
> * 重在带大家了解什么是序列？ 什么是流程图？什么是状态机？
>
> * 流程模板如何使用？
>
> * 流程开发过程如何设置“输入/输出”及“输入/输出加密”
>
> * 什么是RPA系统日志、业务日志？以及如何定义日志级别？不同类型日志的输出位置分别如何查看？
>
> * 如何设置及选择合适的RPA的人机流程交互方式(业务通知&通知方式)
>
> * 如何利用错误处理强壮RPA流程的业务稳定性？

<br><br>

## 一、序列、流程图、状态机区别

首先序列、流程图及状态机都是容器性组件，都可以用来对一些特定组件实现的业务功能进行分组，那么他们之间的区别到底是什么？我们在流程开发时该怎么做区分？接下来分别介绍他们之间的区别：

<br>

### 1.1 什么是序列？

**序列**能够让我们可以将多个组件以线性方式组成流程，也就是说在序列中实现的流程没有箭头指向，流程自上而下运行，业务逻辑简单明了，所以通常用来分组简单的业务流程。

举例如下（序列也是编辑器默认选择和在容器性组件内添加多个组件时自动生成的组件）：

<img width = '300'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide1.jpg"/>

<br>

### 1.2 什么是流程图？

**流程图**则能实现相对复杂逻辑的业务流程，组件之间用连线连接，流程以箭头指向运行，同一个组件在对应的逻辑条件下可执行多次。

举例网页登录场景：通常我们在登录之前需要判断网页是否已登录，如果已登录状态，则不需要输入用户名及密码，即登录模块功能的流程可运行结束，如果还未登录，则需要输入用户名、验证码及点击登录按钮，然后再进行判断是否登录成功，流程示例如下：
<br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide2.jpg"/>

<br><br>

附登录功能流程如下（序列方式）：
<br>

<img width = '200'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide3.jpg"/>

<br><br>

从以上示例可见，当业务需要进行一些逻辑判断规则时，我们采用流程图方式实现会比序列更加清晰明了；当流程没有任何逻辑判断时我们采用序列方式会更加简洁。从整个业务来说，通常流程图中可以包含多个序列组成的功能流程片段。


<br>

### 1.3 什么是状态机？

接下来我们聊聊**状态机**，当一个业务中按同一种逻辑操作后，结果包含两个以上的状态或者多个业务分支情况时，通常用状态机来实现（状态机的具体使用方法可参考[状态机](https://academy.encoo.com/wiki/Activities/WorkflowControl/StateMachine/StateMachine.md)）,当然我们也可以用流程图及流程决策等组件多次判断来开发流程，但这从实现方式及实现后的流程显示方面要比使用状态机复杂且麻烦。

<br>

我们还用登录场景来举例说明，当打开系统后如果有多种状态存在：
1. 登录状态；
2. 输入用户名密码并点击登录后的角色选择状态/页面；
3. 未登录状态。

<br>

使用状态机的登录流程如下所示：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide4.jpg"/>

<br><br>
 
从上图可见，不同的状态设置在不同的转换中，并在该转换下设置对应的登录操作，“未登录”转换如下图所示：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide5.jpg"/>


<br><br><br>

## 二、流程模板

云扩编辑器内置多种流程模板，通常我们在新建项目时选择 “企业流程模板”，该模板已包含了一个完整流程的基本模块：创建日志、环境初始化、数据初始化、主业务处理及结束处理，如下图所示：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide6.jpg"/>

<br><br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide7.jpg"/>

<br><br><br>

## 三、输入/输出

顾名思义，输入是一个业务流程得到预期结果的前提条件，输出则是在有输入的前提下经过一系列业务上的逻辑判断等操作后得出的预期结果。

<br>

### 3.1 输入

通常我们用参数或者配置文件作为流程的输入方式，如果流程开发完成之后由业务人员来操作，那么这两种方式都很容易让业务人员学习与接受，即学习成本很低。

- 用参数作为输入方式，流程运行时会弹出对话框让业务人员输入对应的值，如下图所示：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide8.jpg"/>


<br>

这里顺便说下有哪些信息我们需要作为参数，举个简单的例子：登录一个系统，我们需要用用户名、密码；再比如要读取一个文件中的数据，那么文件路径也是需要我们作为输入的信息。
    
当然在这两个例子中如果用户名、密码还有文件路径永远不变，我们也可以直接作为变量或者固定值写在流程中，但通常不建议这么做，这会给迁移流程或者修改密码等造成一些不必要的麻烦。
    
总而言之，我们把一些可能会发生变化的信息作为输入的参数，在流程运行时填入对应的值，在云扩编辑器中参数的设置方式如下图所示：

<br>
    
<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide9.jpg"/>

- 配置文件作为参数输入，通常推荐用Excel，在Excel中写入一些可能会变化的信息，如上面例子中的用户名、密码、文件路径等，在流程中需要设计读取Excel中输入信息的流程模块。当然具体需要填入哪些信息还要看实际的业务场景，我们只要掌握一个规律：**一些可能会变化的信息**用参数或者配置文件的方式输入，这不仅仅是指在本地会发生变化，也可能因为流程的迁移而导致的变化。

<br>

配置文件格式举例如下（Excel）：
    
<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide10.jpg"/>

<br><br>

那么怎样将配置文件中的信息（输入）读出来以及流程该如何设计？
    
首先，从流程的先后顺序上来说，通常读取配置文件是在业务流程之前；
    
其次，读取方式上来说，我们将配置文件内容用Excel组件“读取区域”读取后存入datatable类变量中存储，后续在业务功能模块中需要时将数据从数据表引用到流程中。举例如下：

<br>
    
<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide11.jpg"/>

<br><br>

- 除了使用简单文本或者配置文件路径作为参数的方式，我们还可以用数据库作为输入的方式，最终要用哪种方式，需要看具体的业务场景及后续的流程运营，如果流程开发完成并上线后，由业务人员来操作，那么推荐用参数或者配置文件，但如果上线后仍然由IT人员运行流程，那么也可以采取用数据库方式，数据库对IT人员来说维护数据更加方便。另外一种情况是客户购买了低代码平台，那么我们也可以使用数据库，这样用户可以在低代平台对数据进行维护。

<br>

### 3.2 输出

输出即流程运行的预期结果或是某个流程功能片段的输出结果，通常根据业务将最终结果存入文件服务、本地excel、数据库或OSS等、或者将结果存到数据库中，而某流程功能片段（子流程）的输出以参数方式传出。

<br>

- 存入文件服务方式流程设计：用“上传文件”组件：（组件具体用法可参考文档[《上传文件》](https://academy.encoo.com/wiki/Activities/Console/FileUploadActivity.md)

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide12.jpg"/>

<br><br>

- 存入本地Excel方式流程设计：用组件“打开/新建“、”写入区域“等（组件具体用法可参考[《写入区域》](https://academy.encoo.com/wiki/Activities/AppAutomation/OfficeExcel/WriteRange.md))

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide13.jpg"/>

<br><br>

- 存入数据库方式流程设计：用组件”连接数据库“、”执行语句“、”插入语句“等（组件具体用法可参考[连接数据库](https://academy.encoo.com/wiki/Activities/Database/ConnectDatabase.md))

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide14.jpg"/>

<br><br><br>

### 3.3 输入/输出加密

通常，输入输出中有些数据是敏感的，需要进行加密方式处理，比如最常见的账号密码，我们在流程开发或者部署时有以下三种方式进行加密：

- 参数类型设置为Password：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide15.jpg"/>

<br><br>

（1）使用”输入密码“组件：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide16.jpg"/>

<br><br>

（2）使用控制台”资产管理“功能进行加密，操作步骤如下：

第1步、从编辑器发布流程至控制台（具体操作方式可参考：[发布自动化项目](https://academy.encoo.com/zh-cn/wiki/Studio/process/PublishProject.md)）
 
第2步、新建资产(具体操作方式可参考:[管理资产](https://academy.encoo.com/zh-cn/wiki/Console/v3.0.x/datacentor/asset/manageAsset.md))

第3步、流程部署（具体操作方式可参考：[流程部署](https://academy.encoo.com/zh-cn/wiki/Console/rpa-center/workflow/manageworkflow.md))

<br><br>

## 四、日志

### 4.1 系统日志

<br>
系统日志是指机器人，编辑器产生的执行日志，一般由云扩研发团队进行技术支持时使用。
- 编辑器，参考（需替换用户）：C:\Users\{user}\AppData\Local\Encoo\Log
- 机器人，在机器人安装目录下，参考：C:\Program Files (x86)\Encoo Robot\Logs

<br><br>

### 4.2 业务日志

业务日志是指设计流程时根据业务的实际情况把一些有必要的信息作为日志来输出，用以后续业务核对或者流程中逻辑及流程运行情况的检查。

日志级别，共有三个选项：Debug, Info, Error，选择其中一项代表后续的编辑器、机器人、控制台能看到的日志信息：

- 选择 Debug 后，可查看最详细的日志信息

- 选择 Info 后，可查看 Info 和 Error 等级的日志信息

- 选择 Error 后，将只输出 Error 日志

<br><br>

### 4.3 如何定义日志级别？

流程的最开始建议调用【设置日志级别】组件，通过输入参数【日志级别】控制流程输出的日志信息，一般情况下，针对RPA开发者建议使用Debug级别。针对流程用户建议使用Info或Error级别。
<br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide17.jpg"/>

<br><br>

**那么什么情况下应该写业务日志？**

- 正常的业务记录日志建议使用Info，针对某些已知的问题（不需要抛出错误），例如没有数据时下载按钮不可见，可以写入日志，以方便后续业务核对。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide18.jpg"/>


- 异常的错误建议使用Error，针对某些未知的错误，例如Catches中的异常，可以把异常日志exception.Message+exception.StackTrace进行输出

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide19.jpg"/>


<br><br>

### 4.4 日志输出位置

（1）**编辑器日志**

**方法1**：流程运行后输出窗口可见日志，可根据界面上的错误、信息、调试进行筛选

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide20.jpg"/>

<br><br>

**方法2**：开始 - 设置 - 项目，勾选【保存运行、调试日志】，打开目录下的日志文件夹

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide21.jpg"/>

<br><br>

（2）**机器人日志**

打开流程库 - 流程包 - 日志

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide22.jpg"/>


<br><br>

点击日志打开文件夹：

<img width = '200'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide22-1.png"/>



- job-xxx.log：记录组件运行日志
- job-xxx-businesslog.log：记录业务日志

<br><br>
 
（3）**控制台日志**

打开控制台-RPA中心-执行记录，查看日志，也可以在此页面的日志级别中筛选对应的级别，例如一般会筛选错误级别的日志，以方便查看流程报错情况。
<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide23.jpg"/>


<br><br>

## 五、通知

### 5.1 业务通知

一般情况下流程运行成功、失败、中间需要人工介入等情况，建议进行通知。

业务通知的方式有短信、邮件、钉钉、企业微信。选择什么样的通知方式取决于用户群体的使用习惯：

- （1）短信方式，目前较多用于银行和政府，相对比较正式，实时性强，而且即使在没有流量的时候依然可以顺利接收

- （2）邮件方式，使用比较广泛，可以发送/抄送给不同的用户，还可携带附件，可以很好进行追溯

- （3）钉钉方式，需要企业中使用钉钉作为沟通工具，实时性强，一般作为通知来使用，比如流程需要人工介入，需要及时在钉钉中进行反馈。或者流程运行成功或者失败，也可以及时通知到用户

- （4）企业微信方式，需要企业中使用企业微信作为沟通工具，说明可参考钉钉方式

<br><br>

### 5.2 通知方式

#### （1）短信通知

短信通知主要是两种方式：

第一种是阿里或者其他平台提供的短信平台，直接调用相关的api接口即可发短信

第二种是需要搭建一个短信平台服务，然后根据平台的接口去调用发送短信

<br><br>

#### （2）邮件通知

邮件通知需要配置邮件发送方的服务器、代理、端口、密码、地址，还需要配置接收方的邮箱、内容、附件。

由于邮件发送服务器或者接收方有可能不稳定，建议放入重试组件中，可以多重试几次，降低失败率。、
<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide24.jpg"/>

<br><br>

#### （3）钉钉/企业微信

**安装消息推送组件**

* 第1步、通过组件市场搜索【消息推送】并进行安装
* 第2步、重新加载项目后，在编辑器组件库消息推送中查看【钉钉消息推送】和【企业微信消息推送】

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide25.jpg"/>




<img width = '300'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide26.jpg"/>

<br><br>

**（4）钉钉消息推送**

简单来说，如果只需要进行消息推送，首先新建一个钉钉群机器人，配置关键词，再把WebHook拷贝到组件，文本里需要包含机器人关键词，这样就可以把对应的文本推送给钉钉群了
<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide27.jpg"/>


如果需要比较复杂的操作，比如需要先接收到用户的消息，根据用户的消息进行流程的处理，最终反馈到钉钉群里。 或者需要反馈到钉钉群里的不单单是文本，还需要有图片或者附件。可以参考完整教程[【案例17】案例详解：钉钉机器人群控&RPA机器人调研](https://www.encoo.com/product-detail/Bg2XkQJb)

<br><br>

**（5）企业微信消息推送**

与钉钉消息推送类似，企业微信也需要先新建一个群机器人，再把WebHook拷贝到组件，这样就可以把对应的文本推送给企业微信群了。具体可参考[【案例16】企业微信自动对话机器人](https://www.encoo.com/product-detail/BQagyZOB)

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide28.jpg"/>

<br><br><br>

## 六、错误处理

在不写Try Catch 的情况下，组件异常会直接中断流程（除非勾选了失败继续），Studio会在输出框打印日志，Robot会对整个屏幕截图，记录日志并中断流程。

**是否应该全局Try Catch？**

需要根据实际情况使用Try Catch，使用全局Try Catch代表需要捕获整体流程的错误：
<br>

- Try中放入整体流程，若try中出现异常，则会进入Catch（可以多个catch 同时存在），在此可以打印日志并通知提示用户出错了，打印消息可参考：exception.Message+exception.StackTrace

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide29.jpg"/>

<br><br>

- Finally可选，若需要可在Finally中释放资源
  <img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/processondesignguide30.jpg"/>  

 

**单独子流程应该catch哪些exception， 应该抛出哪些exception**

- （1）**数据操作中**，循环录入数据的模块中，如果数据之间是相互独立的，所以希望出现异常也继续运行流程，建议使用try catch组件用以捕获因异常数据导致的错误，并且将异常数据进行对应处理（通常会通知用户该数据有异常），同时将异常详情写入业务日志中

- （2）**页面操作中**，最常见的情况是页面没有按预期跳转（未点击到或者网页开小差未响应），接下来的操作会因为未匹配到元素或者等待元素超时而抛出异常中断流程。这时候我们不希望中断流程，可以在Catch/Finally中设置线程休眠30秒，再重新刷新页面

- （3）**关闭可能出现的弹出窗**，例如chrome未正常关闭，下次打开时会有提示恢复页面弹出框，我们希望关闭这个页面。但是这个弹窗并不是一定出现，我们会尝试获取这个元素并点击关闭，这时候需要在外层套一个Try Catch防止抛异常（如弹窗未出现获取元素或点击元素会抛异常），这种情况也可以把组件设定成失败继续

---

#### 附： 更多技术问题加入云扩社区--免费官方技术支持&RPA学习交流

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/12/21/16716261706592.jpg"/>

<font color = 5a6877 size=2 >


[说明] 
* 官方支持时间：工作日 10:00-19:00
* 技术支持老师：云简、云智、云能、云易
* 温馨提示：若同时间问题排队、请稍作等待
 </font>