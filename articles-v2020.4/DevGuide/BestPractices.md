# 指南五《RPA流程开发-最佳实践》

<br>

>导读: 
> 
> 重在带大家了解RPA流程开发时几个企业级RPA流程开发规范需要关注的流程评估维度
> * 维度1：代码(版本)管理
> * 维度2：开发协作与共享规范
> * 维度3：RPA流程数据安全
> * 维度4：流程的稳定与健壮
> * 维度5：流程性能优化
> * 维度6：多流程协作

<br>



## 一、代码管理

RPA项目的工程文件主要包括XAML（流程文件）、Json（配置文件）、各类代码文件（例如cs）和其他引用文件组成（例如Excel文件）。其工程目录可以使用Git等版本控制工具进行版本管理。

当前项目未启用版本控制功能时，单击“启用”，开启版本控制功能，并进行初始化。

</br> <img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/lmx-1.png"/>

</br> 启用后，通过版本控制可以查看工程下的所有文件修改列表，并可以对文件进行回退（放弃修改），对比修改内容，查看历史提交等操作。

具体示例操作见下方图示：

* (1)与未修改的版本比较
</br><img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/lmx-2.png"/> 

* (2)查看历史版本 
</br> <img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/lmx-3.png"/>
</br></br>

> **注意：**
> 
> 针对project.json和project.runtime.json两个配置文件，因开发人员本地编辑器版本不同，会因为本地依赖组件版本不一致导致这两个文件存在大量的编辑冲突，*可添加到gitignore文件中，由团队指定一名成员进行统一的版本维护。*

</br> </br> </br> 

## 二、开发协作与共享
为实现RPA项目开发的团队协助，降低项目后期维护成本，RPA流程设计也需要遵循模块化的设计思路，将公共的业务步骤或可复用的部分抽取成子流程形式，<font color = green>通过调用子流程实现流程步骤的解耦，提升项目的可读性和健壮性。</font>

</br> 

适合抽取子流程的场景大致可按照以下3种情况：
1. 有复用价值的具体业务操作步骤，例如对某个业务系统的登录等。
2. 有复用价值的技术实现功能点，例如对某个日期选择框的操作等。
3. 有一定通用价值且与业务逻辑无关的操作步骤，例如浏览器固定目录下载文件的读取等。
</br>

- 子流程和主流程类似，都是独立的xaml文件，在调用子流程时，主流程和子流程间会存在参数传递以完成信息的交互。

- 在调用子流程组件中配置的调用参数主要包括名称、方向（输入、输出、输入/输出）、类型及值。

- 在子流程文件中的参数列表需要与调用子流程组件设置的参数对应，以接收主流程传递的参数。

- 同理，主流程在接收子流程返回值时，也需要在变量列表中定义变量接收子流程返回的参数并映射到主流程的变量中。具体调用示例可见[《使用参数》-子流程调用参数填写示例](https://academy.encoo.com/zh-cn/wiki/Studio/process/developProject/Arguments/UseArguments.md)



</br><img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/lmx-4.png"/>

</br><img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/lmx-5.png"/>

<br>
<br>

**为什么需要多人协作开发流程？**

当项目多人协同开发时，通过将业务流程进行模块化切分，在主流程中定义不同的子流程步骤，明确每个子流程的实现内容和输入输出参数。

<font color = green>将不同的子流程交由团队的不同成员开发，将极大提升项目整体开发的协同效率，降低因版本配置管理冲突所带来的问题。</font>

流程文件(XAML)作为一种描述性语言，其源码文件并不想程序代码一样容易通过版本管理工具（GIT）进行变更对比。但这不意味着文件对比就无意义，通过编辑器内置的版本对比工具，可以对组件的属性值变更进行对比。

</br><img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/lmx-6.png"/>

</br> </br> </br> 

## 三、安全 ★★★★★
RPA机器人在执行任务过程中，将不可避免的接触到用户的<font color = darkred>敏感信息</font>（例如登录系统的账号密码等）和业务敏感数据（例如财务报表等），以及在运行过程中记录的运行日志等。

针对这些问题，需要RPA产品能力及开发人员在流程设计过程中通过不同的手段来防范这些安全隐患。

1. 针对账号密码等用户敏感信息，不要硬编码在流程文件或配置文件中。**使用控制台的资产管理功能，新建加密存储的数据资产**。在流程中通过获取资产组件来获取所需的敏感信息。
2. 在流程设计开发过程中，将业务敏感数据上传至控制台的文件服务存储，或通过有权限控制的数据库、共享文件夹、FTP等形式进行统一的管理，尽量避免在本地存储业务敏感数据。
3. 在使用日志组件时，利用日志级别对不同信息进行输出。针对敏感信息在UAT或正式上线前检查是否有直接输出日志的内容并进行删除。针对控制台用户实施最小权限原则，仅对RPA开发/运维人员开放运行记录查看功能。

</br> </br> </br> 

## 四、稳定性 ★★★
RPA流程因其代替人工操作的特点，影响运行稳定性的因素较多，主要包含以下几个方面：

1. 环境问题： <font color = green>因RPA部署在Windows桌面环境中，容易受操作系统版本、基础软件版本（例如Chrome浏览器、Excel等）、桌面分辨率甚至输入法等外围因素影响。</font>因此在RPA开发和部署过程中，需尽量保证开发环境和生产部署环境的统一，降低因环境问题造成的流程不稳定因素。

<br>

2. 流程健壮性：流程设计的健壮性是影响运行稳定性最重要的因素，以下几点是最常用的手段：
  </br>-  （1）在流程开始执行时初始化环境，例如关闭浏览器和Excel等影响流程执行的进程。
  </br>-  （2）在使用选择器时善用通配符，兼容不同属性值变化对选择器元素定位造成的影响。
  </br>-  （3）合理设置组件前后延时、执行超时和匹配超时时间，降低因系统或页面加载执行速度对运行稳定性造成的影响。
  </br>-  （4）合理利用Try/Catch组件对可能发生未知问题的步骤进行处理，并及时抛出准确的错误信息。
  </br>-  （5）对于批量运行的任务数据，通过Excel或数据库等准确记录流程运行的处理进度，保证流程可以重复执行，且中断后再执行可以接续运行（检查执行进度，只执行未处理部分）。
  </br>-  （6）通过足够的UAT测试对于系统弹窗或错误提示等无法预期的事件进行验证和针对性处理。

</br> </br> </br> 

## 五、流程性能优化
虽然RPA流程执行是以模拟人工操作为基础实现业务流程，但并不意味完全按照人工操作步骤是最佳执行效率的实现形式。主要可以从RPA操作步骤和组件选择两方面来优化流程执行的性能，提升运行效率。<br><br>

1. 操作步骤优化：
  </br>-  （1）涉及到多系统操作时，尽量在一个系统上完成所有操作或抓取数据后再切换另一个系统，减少因系统切换登录造成的时间损失。
  </br>-  （2）涉及多层级菜单点击切换时，有些过程往往可以通过显式URL跳转形式来快速切换的，减少点击菜单的次数。
  </br>-  （3）在批量数据处理时合理的使用Excel或数据库暂存中间结果，当流程异常中断时，再次执行可从中间步骤接续处理，充分利用之前的执行结果，避免从头开始执行。
  </br>-  （4）在复杂Excel计算处理时，对于需计算的单元格可预先做好公式并保存成模板。RPA运行时打开模板填充原始数据，其余的计算部分交给Excel公式自动刷新。<br><br><br>

2. 合理选择组件：
  </br>-  绝大多数场景下，使用具备批量处理能力的组件都比单一处理的组件效率高。例如使用写入区域组件代替循环写入单元格，使用获取结构化数据组件代替遍历表格DOM结构获取数据。
  </br>-  对于大量复杂的逻辑或数据计算，使用代码处理比操作Excel效率有非常大的提升。
  
</br> </br> </br> 

## 六、多流程协作

在某些场景下，无法通过单一RPA任务完成全部业务操作，或因为流程设计考虑对流程执行步骤进行RPA任务拆分。<br><br>

此时往往需要通过一些机制保证多流程之间的通知机制和数据传递，以实现多流程协作。<br><br>

最主要的实现形式主要有以下两种：<br>
1. 利用控制台的[数据队列](https://academy.encoo.com/wiki/Activities/DevService/Queue/add-message.md)功能，将获取数据和后续业务处理从流程上解耦，以生产者-消费者方式对RPA流程进行切分。这类场景适合获取数据简单但后续业务流程执行耗时长的情况，通过一个获取数据机器人配多个业务处理机器人的形式提升整体的流程执行效率。<br><br>
2. 利用数据库的中间表、FTP监听文件夹或监听邮箱等形式，将RPA任务进行切分，适合无法在单一环境下完成全部任务的场景。通过数据库或文件实现流程间的数据传输和事件触发的监听，实现多流程间的任务协作能力

> **提示**：FTP组件从云扩组件市场组件下载，可用于流程的文件传输 