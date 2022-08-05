# Error<表4>：数据表/数据库



<br><br><br>


### 一、数据表/数据库自动化(报错索引)

<table  border="0" cellpadding="0" cellspacing="0" style="width:756.70pt;border-collapse:collapse;table-layout:fixed;">
   <colgroup><col width="308.65" style="mso-width-source:userset;mso-width-alt:15049;">
   <col width="149.35" span="3" style="mso-width-source:userset;mso-width-alt:7282;">
   </colgroup><tbody><tr height="17" style="height:17.00pt;">
    <td class="xl65" height="17" width="308.65" x:autofilter="all" x:autofilterrange="$A$1:D6" style="height:17.00pt;width:308.65pt;" x:str="">错误信息/错误代码</td>
    <td class="xl66" width="149.35" x:autofilter="all" style="width:149.35pt;" x:str="">索引表</td>
    <td class="xl65" width="149.35" x:autofilter="all" style="width:149.35pt;" x:str="">可能关联事件</td>
    <td class="xl65" width="149.35" x:autofilter="all" style="width:149.35pt;" x:str="">索引编号</td>
   </tr>
   <tr height="51" style="height:51.00pt;">
    <td class="xl67" height="51" style="height:51.00pt;" x:str=""><a href="http://localhost/" target="_parent" title="http://localhost">error 0: Authentication to host 'localhost' for user 'root' using method 'caching_sha2_password' failed with message: Reading from the stream has failed.</a></td>
    <td class="xl68" x:str="">Error&lt;表4&gt;</td>
    <td class="xl68" x:str="">Mysql、连接数据库</td>
    <td class="xl68" x:str="">AC0030</td>
   </tr>
   <tr height="34" style="height:34.00pt;">
    <td class="xl68" height="34" style="height:34.00pt;" x:str="">Loading local data is disabled; this must be enabled on both the client and server sides</td>
    <td class="xl68" x:str="">Error&lt;表4&gt;</td>
    <td class="xl68" x:str="">Mysql、连接数据库</td>
    <td class="xl68" x:str="">AC0031</td>
   </tr>
   <tr height="34" style="height:34.00pt;">
    <td class="xl68" height="34" style="height:34.00pt;" x:str="">无法加载DLL“db2app.dll”：找不到指定的模块（异常来自HRESULT：0x8007007E）</td>
    <td class="xl68" x:str="">Error&lt;表4&gt;</td>
    <td class="xl68" x:str="">Db2、连接数据库</td>
    <td class="xl68" x:str="">AC0032</td>
   </tr>
   <tr height="17" style="height:17.00pt;">
    <td class="xl68" height="17" style="height:17.00pt;" x:str="">连接已经是本地事务处理或分布式事务处理的一部分</td>
    <td class="xl68" x:str="">Error&lt;表4&gt;</td>
    <td class="xl68" x:str="">连接数据库</td>
    <td class="xl68" x:str="">AC0033</td>
   </tr>
   <tr height="51" style="height:51.00pt;">
    <td class="xl68" height="51" style="height:51.00pt;" x:str="">[错误] 执行语句调用去重函数失败。详细错误信息：Fatal error encountered during command execution 少量数据不会报错，六千以上的数据会报错</td>
    <td class="xl68" x:str="">Error&lt;表4&gt;</td>
    <td class="xl68" x:str="">执行语句</td>
    <td class="xl68" x:str="">AC0034</td>
   </tr>
   <!--[if supportMisalignedColumns]-->
    <tr width="0" style="display:none;">
     <td width="309" style="width:309;"></td>
     <td width="149" style="width:149;"></td>
    </tr>
   <!--[endif]-->
  </tbody></table>

<br><br><br>

### 二、具体解决办法

<br>

#### Q：error 0: Authentication to host 'localhost' for user 'root' using method 'caching_sha2_password' failed with message: Reading from the stream has failed.

<font color=5a6877>
<br>

**【解决办法-AC0030】** ：C0030

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0030.jpg"/>

</font>
<br><br>
---
<br>

#### Q：Loading local data is disabled; this must be enabled on both the client and server sides

<font color=5a6877>
<br>

**【解决办法-AC0031】** ：需要在客户端连接字符串设置 AllowLoadLocalInfile=true;服务端设置 SHOW GLOBAL VARIABLES LIKE 'local_infile';SET GLOBAL local_infile = 'ON';<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0031.png"/>


</font>
<br><br>
---
<br>

#### Q：无法加载DLL“db2app.dll”：找不到指定的模块（异常来自HRESULT：0x8007007E）

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0032-1.png"/>

<font color=5a6877>

<br>

**【解决办法-AC0032】** ：步骤如下，
1. 确认Db2扩展是否已经安装，若更新过编辑器或者机器人则需要重新安装Db2扩展
2. Db2 数据库访问驱动DLL需要C++运行时，一般新电脑没有C++运行时，安装即可，链接：连接数据库_数据库
3. 若以上步骤还是提示该问题，需要检查Windows 系统版本，是否是Windows Embedded Standard，根据系统是 64 位系统还是 32 系统下载安装。 
●  [点击下载-安装x64：](https://share.weiyun.com/FFxPWka7)
●  [点击下载-安装x86：](https://share.weiyun.com/DBAnBZBe)

</font>
<br><br>
---
<br>

#### Q：连接已经是本地事务处理或分布式事务处理的一部分

<font color=5a6877>
<br>

**【解决办法-AC0033】** ：检查事务组件是否嵌套事务组件

</font>
<br><br>
---
<br>


#### Q： [错误] 执行语句调用去重函数失败。详细错误信息：Fatal error encountered during command execution   少量数据不会报错，六千以上的数据会报错

<font color=5a6877>
<br>

**【解决办法-AC0034】** ：好像是数据量的问题，试下延长timeout连接字符串和组件，外部调用和内部还是不一样的，一般加“超时”可以解决 

</font>
<br><br>
---
<br>

