# Error5：邮件相关

<br>


#### Q：Outlook邮件登录，错误代码CAA20002 

<br>

<font color=5a6877>
<br><br>

**【解决办法-AC0048】**:

1、停止使用VPN 
2、更改MS团队密码
3.在Windows中添加MS团队帐户
4、要求改变政策
5.清除MS团队的缓存文件
卸载并重新安装MS团队

Teams caa20002, Outlook autodiscover bonks. Where to look, what to do?
https://www.reddit.com/r/Office365/comments/pl1kkf/teams_caa20002_outlook_autodiscover_bonks_where/

So, What is Microsoft Team’s error code caa20002?https://10scopes.com/fix-microsoft-teams-error-code-caa20002/

</font>
<br><br>
---
<br> 
 

#### Q：获取邮件信息失败。

<font color=5a6877>
<br>

**【解决办法-AC0034】**：

查看是否配置了邮箱的账户信息，如果配置了邮箱名称（不是邮箱地址，见图1），使用邮箱名称填写获取邮件
<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0034-1.png"/> 
<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0034-2.png"/>


</font>
<br><br>
---
<br>

#### Q：发送邮件失败。535: Login Fail. Please enter your authorization code to login.

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0035.png"/>


<font color=5a6877>

<br>

【原因分析】：
- 可能1：账密填写错误，注意此处的密码不是填写登入密码，而是授权码，详见链接：[QQ邮箱授权码如何获取？](https://jingyan.baidu.com/article/ac6a9a5eb439f36b653eacc0.html)
- 可能2：系统规则判定，对同一个账号发送太多邮件，触发了邮件的广告邮件或垃圾邮件机制，限制了发送。

<br>

**【解决办法-AC0035】**：

* 方法1：再次确认一下，账号和密码有没填错；
* 方法2：修改用户配置 选现=》信任中心=》信任中心设置=》编程访问，选择从不向我发出警告的选项

</font>
<br><br>
---
<br>

#### Q：连接服务器失败

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0036.jpg"/>

<font color=5a6877>
<br>

**【解决办法-AC0036】** ：查看自己邮箱设置里面的smtp配置（参考163的配置，如图5），通常私有的邮箱服务器会自己配置smtp,pop3等服务，需要联系自己公司邮箱管理员查询相关信息了；

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0036-1.png"/>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0036-2.png"/>



</font>
<br><br>
---
<br>


#### Q：[错误]Outlook的COM端口被占用，请检查是否有插件占用改端口或者关闭Outlook客户端。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0037.png"/>


<font color=5a6877>
<br>

**【解决办法-AC0037】** ：Outlook的配置信息截个图，提示端口被占用（环境问题）客户关闭客户端重启就好）。

</font>
<br><br>
---
<br>
