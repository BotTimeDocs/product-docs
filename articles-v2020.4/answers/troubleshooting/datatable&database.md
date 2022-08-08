# Error<表4>：数据表/数据库



<br><br><br>


### 一、数据表/数据库自动化(报错索引)

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-wa1i{font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-uzvj{border-color:inherit;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-7h26{color:#00E;text-align:left;text-decoration:underline;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 466px">
<colgroup>
<col style="width: 262px">
<col style="width: 137px">
<col style="width: 67px">
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
    <td class="tg-7h26"><a href="http://localhost/">error 0: Authentication to host 'localhost' for user 'root' using method 'caching_sha2_password' failed with message: Reading from the stream has failed.</a></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Mysql、连接数据库</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0030</span></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Loading local data is disabled; this must be enabled on both the client and server sides</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Mysql、连接数据库</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0031</span></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">无法加载DLL“db2app.dll”：找不到指定的模块（异常来自HRESULT：0x8007007E）</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Db2、连接数据库</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0032</span></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">连接已经是本地事务处理或分布式事务处理的一部分</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">连接数据库</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0033</span></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">[错误] 执行语句调用去重函数失败。详细错误信息：Fatal error encountered during command execution 少量数据不会报错，六千以上的数据会报错</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">执行语句</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">AC0034</span></td>
  </tr>
  
</tbody>
</table>

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

