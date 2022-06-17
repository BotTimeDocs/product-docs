# 什么是控制台
控制台是自动化业务的统一管控中心，资源管理、流程调度、日志跟踪、低代应用、统计报表、监控和报警、AI的集合。以资源组作为资源的管理单位，支持用户跨资源组访问。使用控制台，可以轻松完成RPA自动化业务的企业级运维。
# 控制台的组成
## 流程库
来自各个部门、各个业务条线的流程开发者，将设计好的流程发布到控制台，构成了流程库。 
>流程，即以dgs为后缀的流程包文件，是RPA自动化业务运行最原子、最核心的执行资源。

流程库的来源有2个：

- 由开发者从编辑器端发布流程
![consoleintroduction1](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction1.jpg)

- 由开发者或IT运维上传本地流程
![consoleintroduction2](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction2.jpg)

## 机器人管理
机器人作为RPA自动化流程的执行载体，可以模拟人正常的界面端或是移动端操作，管理员可以下发一个流程到机器人客户端上执行。用户可通过控制台首页下载机器人安装包，将机器人客户端安装到本机电脑，并通过”账号激活“的方式，与控制台建立连接，受控制台统一管控。

机器人客户端激活的方式有2种：
- 账号激活，通用方式，推荐，与控制台连接，受控制台调度
- 许可证激活，不推荐，机器码+许可证号，一对一激活，无控制台，不建议企业级用户使用

**机器人组**支持机器人资源的最大化利用，一个流程可以下发给一个机器人组，自动从组里选择一个可用的机器人执行任务，避免资源空闲、独占。

## 流程调度
流程调度，即在不同场景、不同形式下，下发流程到机器人执行。触发流程调度的方式有如下几种：

- 手动，用户创建一个流程部署，将流程包和机器人建立起联系，当手动触发时，控制台会立即下发流程执行任务到机器人/机器人组。
- 定时，用户创建一个流程部署，同时设置一个定时任务，而控制台会根据定时任务生成的执行时间，到达执行时间时，则立即下发流程执行任务到机器人。
>请阅读有关[定时任务](https://academy.encoo.com/zh-cn/wiki/Console/rpa-center/workflow/trigger.md?uuid=58257e0f-2bb3-4355-8920-9793b1cec1a4)的更多内容。

![consoleintroduction3](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction3.jpg)

- 任务队列，基于消息的生产/消费机制，一方面向队列里放入消息，另一方面从队列里消费消息，而每当消费一条任务消息，则会触发一次流程任务执行。
>请阅读有关[任务队列](https://academy.encoo.com/zh-cn/wiki/Console/rpa-center/taskqueue/taskqueue.md?uuid=2f5cce8e-5bc7-4da3-bd09-9e950dd481d6)的更多内容。

![consoleintroduction4](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction4.jpg)

- 流程编排，一般用于复杂场景，将多个流程部署按照顺序编排起来，触发编排即触发多个流程部署串行执行，支持定时任务、手动触发流程编排执行。

>请阅读有关[流程编排](https://academy.encoo.com/zh-cn/wiki/Console/rpa-center/flowSequence/aboutFlowSequence.md)的更多内容。


**调度方式举例**
1. 若一个流程部署里，流程关联1个机器人，则1个流程执行任务只会下发给这1个机器人执行；
2. 若一个流程部署里，流程包关联多个机器人，则1个流程执行任务会同时下发给多个机器人执行；
3. 若一个流程部署里，流程关联1个机器人组，机器人组里有5个可用的机器人，则1个流程执行任务会从组里任选1个可用的机器人执行。

**任务在机器人上排队**
当多个流程执行任务下发给同一个机器人执行，同一个优先级的任务，则按照”先来先到“策略；不同优先级的任务，则优先级高的先执行。

优先级（1-5000）：优先级越高，则任务越优先执行。

优先级设置？
 
>更多关于流程调度的细节， 请参见：[流程运行管理](https://dev-academy.bottime.com/zh-cn/wiki/RunManager/ProcessRunManager.md)

## 流程运行监控和报警
流程运行时，一方面控制台可实时监控流程日志，另一方面机器人所在的计算机情况，控制台也会实时监控，并根据预警策略发出邮件警报。 

例如内存使用率过高、CPU使用率过高、机器人状态为中断时。

- 实时日志监控
![consoleintroduction5](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction5.jpg)

- 机器人预警配置
![consoleintroduction6](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction6.jpg)

- 监控机器人所在计算机性能
![consoleintroduction7](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction7.jpg)

>更多运行监控细节， 请参考[流程运行管理](https://dev-academy.bottime.com/zh-cn/wiki/RunManager/ProcessRunManager.md)

## 开发服务
### 文件

文件服务为RPA开发人员提供了各类文件的存储解决方案。 支持对文件夹的增删改以及文件的上传、下载等功能。 在RPA流程中可直接使用或更新文件服务中的数据。

此外，通过数据权限配置可以来控制用户对这些文件/文件夹的访问，使之仅限所需要的用户使用。
![consoleintroduction8](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction8.jpg)

### 资产

资产通常表示可在不同自动化项目或同一流程的多次执行时，所使用的共享变量或凭据。它们允许您存储特定信息，以便RPA流程轻松访问。

资产分为以下五种类型：
-  账户凭证密码：包含机器人执行特定流程所需的用户名和密码
    - 例如，SAP 或 SalesForce 的登录详细信息。

- 布尔型：支持值True或False
 
- 字符串：仅存储文本（无需添加双引号）

- 整型：仅存储整数

- 浮点型: 仅存储小数
![consoleintroduction9](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction9.jpg)


还应该讲一下资产enable开发者和IT之间的协作，生产环境



### 连接器
连接器可以打通外部应用数据或调用外部应用开放的服务，例如：MySql、SqlServer、AzureBlob等。

开发者只需要对连接器完成授权或少量填写一些配置信息，即可与对应产品建立连接，从而进行各类数据操作，轻松实现数据互联互通。
![consoleintroduction10](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/introduction10.jpg)


### 组织与权限
用户、角色、部门构建起组织与权限的关系。一个用户在一个部门拥有什么角色，决定了用户对此部门下各类资源数据的操作权限。

组织一般可以基于现实中公司部门架构，由公司管理员创建。公司管理员可以邀请新用户到组织的某个部门，并赋予新用户对此部门的访问角色。

控制台提供了通用的内置角色，如公司管理员、部门管理员，同时也支持用户创建自定义角色。

用户通过SaaS控制台自主注册成为社区版用户；也可申请转为企业版用户，企业版用户可通过邀请机制创建组织架构。

# 私有化控制台
私有化控制台指部署在企业内网或企业指定环境的控制台， SAAS控制台是云扩维护的直接注册即可使用。 这两种方式部署的控制台， 绝大部分功能是完全一致的。 

**当您有如下情况时，推荐使用私有化控制台**
1. 客户希望企业内部定制系统，如logo、跨平台流程调度等；
2. 客户有运维团队，希望自己运维，数据本地存储，基于安全、内部沟通成本低等；
3. 公司业务在局域网，选择私有化部署，如国企、银行等；
4. 政策要求，同时对数据安全要求高，如大型国企、银行；

**当您有如下情况时，推荐使用SAAS控制台**
1. 业务简单，不用投入运维成本；
2. 业务有一定体量、复杂度，但客户无IT部门，只有业务部门，如零售业；
3. 对数据安全的等级要求不高，同时数据存储方式灵活，支持公有云和私有云；

>了解更多， 请参见[私有化指南](https://dev-academy.bottime.com/zh-cn/wiki/RunManager/EnterpriseOM.md)