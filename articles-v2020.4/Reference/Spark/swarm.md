<table width="824.25" border="0" cellpadding="0" cellspacing="0" style="width:824.25pt;border-collapse:collapse;table-layout:fixed;">
   <colgroup><col width="48" span="2" style="width:48.00pt;">
   <col width="152.50" style="mso-width-source:userset;mso-width-alt:7435;">
   <col width="121.60" style="mso-width-source:userset;mso-width-alt:5929;">
   <col width="206.65" style="mso-width-source:userset;mso-width-alt:10076;">
   <col width="247.50" style="mso-width-source:userset;mso-width-alt:12068;">
   </colgroup><tbody><tr height="16.80" style="height:16.80pt;">
    <td class="xl65" height="16.80" width="48" style="height:16.80pt;width:48.00pt;"></td>
    <td class="xl65" width="48" style="width:48.00pt;"></td>
    <td class="xl65" width="152.50" style="width:152.50pt;"></td>
    <td class="xl65" width="121.60" style="width:121.60pt;" x:str="">最低配置</td>
    <td class="xl65" width="206.65" style="width:206.65pt;" x:str="">推荐配置</td>
    <td class="xl73" width="247.50" style="width:247.50pt;" x:str="">备注</td>
   </tr>
   <tr height="56" style="height:56.00pt;mso-height-source:userset;mso-height-alt:1120;">
    <td class="xl66" height="415" rowspan="11" style="height:415.00pt;border-right:.5pt solid #000000;border-bottom:none;" x:str="">控制台</td>
    <td class="xl67" colspan="2" style="border-right:.5pt solid #000000;border-bottom:.5pt solid #000000;" x:str="">硬件要求<br>（高可用方案最低3台服务器节点）</td>
    <td class="xl68" x:str="">4 CPU<br>8 GB 内存<br>100 GB 空闲磁盘</td>
    <td class="xl68" x:str="">8 CPU<font class="font1"><br></font><font class="font1">16 GB内存</font><font class="font1"><br></font><font class="font1">200 GB 空闲磁盘</font></td>
    <td class="xl73"></td>
   </tr>
   <tr height="76" style="height:76.00pt;mso-height-source:userset;mso-height-alt:1520;">
    <td class="xl66" rowspan="10" style="border-right:.5pt solid #000000;border-bottom:none;" x:str="">软件要求</td>
    <td class="xl65" x:str="">操作系统</td>
    <td class="xl69" colspan="2" style="border-right:.5pt solid #000000;border-bottom:.5pt solid #000000;" x:str="">CentOS 7.4及以上或linux内核版本在4.0以上的Linux发行版</td>
    <td class="xl73"></td>
   </tr>
   <tr height="100" style="height:100.00pt;mso-height-source:userset;mso-height-alt:2000;">
    <td class="xl65" x:str="">端口开放</td>
    <td class="xl70" colspan="2" style="border-right:.5pt solid #000000;border-bottom:.5pt solid #000000;" x:str="">控制台前端站点 console-web-v4， 默认端口 80<font class="font1"><br></font><font class="font1">低代前端站点 apps-web，默认端口 82</font><font class="font1"><br></font><font class="font1">单点登录站点 identity-service，默认端口 81</font><font class="font1"><br></font><font class="font1">接口网关站点 apigateway-service，默认端口 8080</font><font class="font1"><br></font><font class="font1">对象存储服务 默认端口9000</font><font class="font1"><br></font><font class="font1">Swarm集群之间通信端口： 2377 7946 4789</font></td>
    <td class="xl73"></td>
   </tr>
   <tr height="33" style="height:33.00pt;mso-height-source:userset;mso-height-alt:660;">
    <td class="xl65" rowspan="3" style="border-right:.5pt solid #000000;border-bottom:.5pt solid #000000;" x:str="">访问入口负载均衡</td>
    <td class="xl71" colspan="2" rowspan="3" style="border-right:.5pt solid #000000;border-bottom:none;" x:str="">1.域名访问；2. 域名+端口访问；3.IP+端口访问； （以上三种访问方式，都需要配置好转发策略）（第一种域名访问方式，需要申请五个一级域名（控制台前端服务，授权认证服务，对象存储服务；API网关接入服务，小程序web前端服务）（第二种访问方式，至少需要申请一个域名）</td>
    <td class="xl77" rowspan="3" style="border-right:.5pt solid #000000;border-bottom:none;"></td>
   </tr>
   <tr height="33" style="height:33.00pt;mso-height-source:userset;mso-height-alt:660;">
   </tr><tr height="33" style="height:33.00pt;mso-height-source:userset;mso-height-alt:660;">
   </tr><tr height="16.80" style="height:16.80pt;">
    <td class="xl65" x:str="">NFS服务</td>
    <td class="xl72" colspan="2" style="border-right:none;border-bottom:.5pt solid #000000;" x:str="">集群节点挂载NFS服务共享目录，共享部署文件</td>
    <td class="xl78" x:str="">非必须，用于提供统一的部署文件和日志存储</td>
   </tr>
   <tr height="16.80" style="height:16.80pt;">
    <td class="xl65" x:str="">对象存储服务</td>
    <td class="xl72" colspan="2" style="border-right:none;border-bottom:.5pt solid #000000;" x:str="">兼容S3接口的对象储存（需要配置跨域策略）</td>
    <td class="xl73"></td>
   </tr>
   <tr height="16.80" style="height:16.80pt;">
    <td class="xl69" x:str="">mysql服务</td>
    <td class="xl70" colspan="2" style="border-right:.5pt solid #000000;border-bottom:.5pt solid #000000;" x:str="">Mysql 5.7及以上版本</td>
    <td class="xl73"></td>
   </tr>
   <tr height="16.80" style="height:16.80pt;">
    <td class="xl69" x:str="">redis服务</td>
    <td class="xl72" colspan="2" style="border-right:none;border-bottom:.5pt solid #000000;" x:str="">Redis4.x及以上版本</td>
    <td class="xl73"></td>
   </tr>
   <tr height="16.80" style="height:16.80pt;">
    <td class="xl73" x:str="">容器注册表</td>
    <td class="xl74" colspan="2" style="border-right:none;border-bottom:.5pt solid #000000;" x:str="">上传镜像到容器注册表，供服务器下载控制台镜像</td>
    <td class="xl73" x:str="">非必须，用于提供镜像存储服务</td>
   </tr>
   <tr height="16.80" style="height:16.80pt;">
    <td height="16.80" style="height:16.80pt;"></td>
    <td class="xl75" colspan="5" style="mso-ignore:colspan;"></td>
   </tr>
   <tr height="16.80" style="height:16.80pt;">
    <td height="16.80" style="height:16.80pt;"></td>
    <td class="xl75" colspan="5" style="mso-ignore:colspan;"></td>
   </tr>
   <tr height="16.80" style="height:16.80pt;">
    <td class="xl76" height="16.80" colspan="3" style="height:16.80pt;border-right:none;border-bottom:none;" x:str="">注：除标注了【非必须】的条目，其他须由客户提<span style="display:none;">供</span></td>
    <td class="xl75" colspan="3" style="mso-ignore:colspan;"></td>
   </tr>
   <!--[if supportMisalignedColumns]-->
    <tr width="0" style="display:none;">
     <td width="153" style="width:153;"></td>
     <td width="122" style="width:122;"></td>
     <td width="207" style="width:207;"></td>
     <td width="248" style="width:248;"></td>
    </tr>
   <!--[endif]-->
  </tbody></table>