### 一、控制台-报错索引

|序号|  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;错误信息&错误代码 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|可能关联事件|解决办法(编号)
|---|---|---|---|
1|未知异常|控制台机器人激活|C0001
2|机器人未授权，请在控制台绑</br>定许可后重新连接  |控制台机器人激活|C0002
3|服务器内部异常|控制台机器人激活|C0003
<br>


###  二、具体解决办法

</br>
</br>

#### 【报错异常】 V3版本控制台，机器人激活显示：未知异常。


![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/解决办法-C0001.png)

</br>
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
