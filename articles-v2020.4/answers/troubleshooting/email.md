# Error<表5>：邮件相关

<br>
<br>


### 一、邮件相关(报错索引)

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-wa1i{font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-bzb2{color:#00E;text-align:left;text-decoration:underline;vertical-align:middle}
.tg .tg-uzvj{border-color:inherit;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 425px">
<colgroup>
<col style="width: 253px">
<col style="width: 96px">
<col style="width: 76px">
</colgroup>
<thead>
  <tr>
    <th class="tg-uzvj"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">错误信息/错误代码</span></th>
    <th class="tg-wa1i"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">可能关联事件</span></th>
    <th class="tg-wa1i"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">索引编号</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-bzb2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">获取邮件信息失败</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">获取邮件</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0034</span></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">发送邮件失败。535: Login Fail. Please enter your authorization code to login.</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">发送邮件</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0035</span></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">连接服务器失败</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">获取邮件</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0036</span></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">[错误]Outlook的COM端口被占用，请检查是否有插件占用改端口或者关闭Outlook客户端。</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">获取邮件</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0037</span></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">[错误] 执行语句调用去重函数失败。详细错误信息：Fatal error encountered during command execution 少量数据不会报错，六千以上的数据会报错</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal">获取邮件</span></td>
    <td class="tg-0lax"><br>AC0034<br></td>
  </tr>
</tbody>
</table>
  
<br>


### 二、具体解决办法

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
