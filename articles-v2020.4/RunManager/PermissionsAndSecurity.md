# 管理4、《权限与安全》

<br> 

>  导读 : 
> 
> 本章指南，重在介绍许可证的不同类型包括：编辑器/机器人许可(固定许可VS浮动许可）、vicode应用许可、文档理解模板许可、个人版许可证；
> 
> 以及控制台种的组织架构管理相关概念，包括租户、部门、用户及对应的邀请与激活操作。
> 
<br> <br> <br> 

## 一、许可证

许可证，即授权编辑器、机器人正常运行的许可，同时也授权vicode应用上架、文档理解模板发布的许可。

<br> 

### 1.1 编辑器/机器人许可(固定许可VS浮动许可）

#### （1）编辑器之固定许可
每当登录一台编辑器，你将会占用一个编辑器的许可数量。

**占用许可**
当你用控制台账号登录你的编辑器时, 将在许可证页面占用一个相应版本的编辑器许许可证。登录成功后，许可证的企业版编辑器将显示已使用数量+1。同时可以在“查看使用情况”列表中查看使用的用户以及机器名称。

常规路径：编辑器启动->编辑器登录->编辑器检查当前计算机+用户许可证情况->编辑器尝试绑定许可证

<br> 

> **说明：**
> 控制台的编辑器名额采用”抢占制“，租户下的所有账户均可登录编辑器占用许可，采用先登录先占用，占满为止的策略。
> 

<br> <br> 

![编辑器之固定许可](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-permit01.png)


<br> <br> 

**释放许可**
当你想要释放一些被占用的编辑器许可额度，以供后续其他用户使用时，你可以采取两种方式释放名额。

1. 在编辑器的右上角找到“用户人像”图标，点击 退出登录。退出成功后，本台机器占用的编辑器额度即刻释放。
2. 在 “全局管理 > 许可证”页面中，点击“查看使用情况”，找到想要释放的名额，点击“移除许可”，占用的编辑器额度即刻释放。 对应的编辑器将在下一次检查许可证时自动登出。

<br> <br> 

#### （2）编辑器之浮动许可
浮动许可证具备很强的灵活性，其支持共享使用，可在不同的计算机间进行转移，但同一时刻可以使用的授权总数量不超过允许的上限。

常规路径：编辑器启动->编辑器登录->编辑器检查当前计算机+用户许可证情况->编辑器尝试绑定许可证

**相较于固定许可，浮动许可编辑器，关闭时会解绑许可，释放资源。**

<br> <br> 

> **说明：**
> 浮动许可证应用场景示例： 银行中，安装 100 个机器人，但许可证仅购买 50 个的时候，如果使用固定的许可证，一个机器人必须绑定一个许可证，且不需要使用时
> 
> 需手动解绑，使用起来较为繁杂。此时，浮动许可尤为重要，当机器人执行时可获取许可，执行完成则可将许可释放，许可证的灵活性使机器人的利用率大大提升。

<br> <br> 

#### （3）机器人之固定许可
每当用户在控制台，新增一个机器人会消耗一个机器人许可，注意：浮动许可，只有机器人运行时才会占用许可。

<br> 


<br> <br> <br> 

**占用许可**

当你在控制台新增机器人时，新增一个机器人，则会在许可证页面看到已占用固定许可额度。例如，你在控制台新增了一个企业版机器人，新增成功后，许可证的企业版机器人将显示已使用数量+1。

常规路径：控制台创建机器人->控制台绑定许可证->客户端机器人连接->执行流程

> **说明：**
>当占用的名额到达许可上限时，则无法再新增该类型的机器人，已经新增的机器人可以正常使用。

![机器人之固定许可](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-permit02.png)


<br> <br> <br> 

**释放许可**

当你想要释放一些被占用的机器人许可额度，以供后续用户使用时，你可以采取两种方式释放许可：
1. 在“机器人管理”页面中，选择需要被释放的机器人，点击对应的“移除许可”链接，可移除该机器人身上的许可证。
2. 在 “全局管理 > 许可证”页面中，点击“查看使用情况”，找到想要释放的名额，点击“移除许可”即可移除该机器人身上的许可证。
> **说明：**
>释放机器人的固定许可，一般为用户主动发起。

<br> <br> <br> 

#### （4）机器人之浮动许可
在“机器人管理”页面，新增机器人时，支持选择新增“企业版固定许可证”和“企业版浮动许可证”。当检测到当前为浮动许可证时，机器人连接控制台不占用许可证，直接进入。

**机器人仅在执行流程时，需要获取许可证**

1. 执行前，机器人自动获取浮动许可证并绑定。
2. 执行过程中，机器人断开时，中断执行并自动解绑许可证。
3. 执行完成后，机器人自动解绑许可证。

常规路径：控制台创建机器人->机器人客户端连接控制台->执行任务前，机器人客户端请求占用许可证->执行流程->执行完成后，机器人客户端请求释放许可证

<br> <br> <br> 

### 1.2 vicode应用许可
开发并上架 一个ViCode 应用，“已上架”的ViCode 应用，会占用许可，即当上架一个应用，则”许可证管理“下许可的“已绑定量”会+1。
同时，用户亦可在”许可证管理“下移除应用，进而收回一个许可。

![vicode应用许可](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-permit03.png)

<br> <br> <br> 

### 1.3 文档理解模板许可
许可证主要用于控制文档理解模板的可调用次数, 目前按照内置模型种类进行控制。

![AI文档理解许可](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-permit04.png)

<br> <br> <br> 

### 1.4 个人版许可证
当用户注册个人版账户，将获取一个个人版控制台，一个个人版编辑器，一个个人版机器人，一个低代app上架的使用权。

个人版许可证将不会失效。如果你超过一年未登陆控制台，你的账户可能会被回收，默认回收后不做另行通知。

<br> <br> <br> 

## 二、组织架构管理
组织架构管理主要用于对公司中的部门、用户进行管理，同时可对相关部门、用户、机器人的各类权限进行控制。

### 2.1 租户
用户在控制台注册一个账号，系统会根据填写的信息自动生成一个租户，账户默认属于当前租户。

<br> 

同时，SaaS控制台支持多租户模式，即一个账户可以被邀请到多个租户下，如账户（123@sina.com），同时是租户(云扩科技)和租户（讯飞科技）的用户，用户登陆时，可选择任意一个租户进入。

<br> <br> 

### 2.2 部门
当一个企业级控制台，创建了一个租户，公司管理员会根据实际的业务部门创建组织架构部门，以便邀请新用户到控制台时，选择对应部门，便于用户管理。

<br> <br> 

### 2.3 用户
即一个自然人，一个用户在控制台拥有一个账号，登录控制台后，可进行一些列操作。

<br> <br> 

### 2.4 邀请与激活
SaaS控制台组织架构的创建，基于邀请和激活。

首先，公司管理员通过控制台邀请一个新用户到当前租户下，录入邀请人邮箱、部门、角色，系统会发送一份邮件。

然后，新用户登录邮箱服务，点击邮件里的激活连接，设置登录密码，登录控制台。

<br> 

#### 2.4.1 云扩控制台构建组织架构

（1）SaaS云扩控制台(个人版)，用户自主注册，即可称为个人版用户，个人版控制台为一个租户+一个用户的默认模式，不支持构建多用户的组织架构。

（2）SaaS云扩控制台（企业版），当一个社区用户申请称为企业用户，就可以构建组织架构，即一个企业租户下邀请多个用户到当前租户下。SaaS控制台支持多租户模式。

（3）私有化云扩控制台，一般情况，私有化控制台的组织架构由租户的公司管理员统一创建并管理，亦可根据客户的私有化环境情况，选择是否支持邮箱和短信服务。私有化控制台，目前仅支持单租户模式。

<br> <br> 

#### 2.4.2 集成第三方组织架构

<br><br>

**教程1：同步企业微信组织架构到控制台**

<br>

第1步：企业微信管理员打开[企业微信管理后台](https://work.weixin.qq.com/wework_admin/loginpage_wx)，并扫码登录

![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin01.png)
    
![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin02.png)

![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin03.png) 

![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin04.png)
       
<br><br><br>

第2步：打开应用管理-应用-云扩低代码
![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin05.png)
  
  <br><br><br>              

第3步：修改用户可见范围，此处当企微组织架构发生变动，控制台组织架构同步变动
        
![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin06.png)

![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin07.png)

![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin08.png)
                

<br><br><br>
      

**如何新增一个部门？？**

首先企业微信管理员将新部门添加到可见范围（见3-修改用户可见范围），然后公司管理员登录云扩控制台刷新组织架构。

当原有部门或人员变动，管理员刷新组织架构即可。

![企业微信](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-weixin09.png)
        
        

     