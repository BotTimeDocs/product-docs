<table width="923.20" border="0" cellpadding="0" cellspacing="0" style="width:923.20pt;border-collapse:collapse;table-layout:fixed;">
   <colgroup><col width="99.55" style="mso-width-source:userset;mso-width-alt:4247;">
   <col width="67.20" style="mso-width-source:userset;mso-width-alt:2867;">
   <col width="133" style="mso-width-source:userset;mso-width-alt:5674;">
   <col width="184.15" style="mso-width-source:userset;mso-width-alt:7857;">
   <col width="165.50" style="mso-width-source:userset;mso-width-alt:7061;">
   <col width="273.80" style="mso-width-source:userset;mso-width-alt:11682;">
   </colgroup><tbody><tr height="24" style="height:24.00pt;mso-height-source:userset;mso-height-alt:480;">
    <td class="xl65" height="24" width="299.75" colspan="3" style="height:24.00pt;width:299.75pt;border-right:1.0pt solid windowtext;border-bottom:1.0pt solid windowtext;"></td>
    <td class="xl65" width="184.15" style="width:184.15pt;" x:str="">node节点最低配置<span style="mso-spacerun:yes;">&nbsp;</span></td>
    <td class="xl65" width="165.50" style="width:165.50pt;" x:str="">node节点推荐配置</td>
    <td class="xl65" width="273.80" style="width:273.80pt;" x:str="">备注</td>
   </tr>
   <tr height="54" style="height:54.00pt;mso-height-source:userset;mso-height-alt:1080;">
    <td class="xl67" height="487.35" rowspan="8" style="height:487.35pt;border-right:none;border-bottom:1.0pt solid windowtext;" x:str="">控制台 Console<br>（含ViCode）</td>
    <td class="xl68" colspan="2" style="border-right:.5pt solid windowtext;border-bottom:.5pt solid windowtext;" x:str="">硬件要求<br>（K8S高可用方案最低3台node节点）</td>
    <td class="xl70" x:str="">8核 CPU<br>16GB 内存<br>100GB 空闲磁盘</td>
    <td class="xl70" x:str="">16核 CPU或更高<br>32GB 内存或更高<br>100GB 以上空闲磁盘</td>
    <td class="xl85"></td>
   </tr>
   <tr height="93" style="height:93.00pt;mso-height-source:userset;mso-height-alt:1860;">
    <td class="xl71" rowspan="7" style="border-right:.5pt solid windowtext;border-bottom:1.0pt solid windowtext;" x:str="">软件要求</td>
    <td class="xl72" x:str="">K8S命名空间</td>
    <td class="xl73" colspan="2" style="border-right:.5pt solid windowtext;border-bottom:.5pt solid windowtext;" x:str="">一个独立的命名空间</td>
    <td class="xl86" x:str="">如果命名空间使用了LimitRange，limits每个pod至少为0.5core 2G<br><br>如果命名空间使用ResourceQuota， 命名空间ResourceQuota配额request/limits总额至少不低于控制台所有pod的request/limits总和</td>
   </tr>
   <tr height="31.15" style="height:31.15pt;mso-height-source:userset;mso-height-alt:623;">
    <td class="xl75" x:str="">对象存储服务</td>
    <td class="xl76" colspan="2" style="border-right:.5pt solid windowtext;border-bottom:.5pt solid windowtext;" x:str="">兼容S3接口的对象储存（需要配置跨域策略）</td>
    <td class="xl88"></td>
   </tr>
   <tr height="37.15" style="height:37.15pt;mso-height-source:userset;mso-height-alt:743;">
    <td class="xl73" x:str="">mysql服务</td>
    <td class="xl77" colspan="2" style="border-right:.5pt solid windowtext;border-bottom:.5pt solid windowtext;" x:str="">Mysql 5.7及以上版本</td>
    <td class="xl88"></td>
   </tr>
   <tr height="37.15" style="height:37.15pt;mso-height-source:userset;mso-height-alt:743;">
    <td class="xl78" x:str="">redis服务</td>
    <td class="xl76" colspan="2" style="border-right:.5pt solid windowtext;border-bottom:.5pt solid windowtext;" x:str="">Redis4.x及以上版本</td>
    <td class="xl89" x:str="">支持单机/主从/哨兵模式，不支持集群模式。</td>
   </tr>
   <tr height="25.90" style="height:25.90pt;mso-height-source:userset;mso-height-alt:518;">
    <td class="xl76" x:str="">镜像存储服务</td>
    <td class="xl76" colspan="2" style="border-right:.5pt solid windowtext;border-bottom:.5pt solid windowtext;" x:str="">例如harbor，ACR等</td>
    <td class="xl88" x:str="">上传控制台镜像到镜像仓库，供kubernetes下载</td>
   </tr>
   <tr height="126" style="height:126.00pt;mso-height-source:userset;mso-height-alt:2520;">
    <td class="xl79" x:str="">访问方式</td>
    <td class="xl80" colspan="2" style="border-right:.5pt solid windowtext;border-bottom:1.0pt solid windowtext;" x:str="">通过ingress暴露服务(ingress-nginx)<span style="mso-spacerun:yes;">&nbsp; </span><br><br>浏览器通过域名访问控制台，需要申请四个域名<br>1.控制台前端站点域名 2.低代前端站点域名<br>3.单点登录站点域名 4.接口网关站点域名<br><br>确定访问协议是http还是https</td>
    <td class="xl86" x:str="">云扩RPA控制台相关的服务均承载在K8S集群中，服务通过ingress将内部服务暴露出来供外部访问</td>
   </tr>
   <tr height="83" style="height:83.00pt;mso-height-source:userset;mso-height-alt:1660;">
    <td class="xl83" x:str="">其它要求</td>
    <td class="xl80" colspan="2" style="border-right:.5pt solid windowtext;border-bottom:1.0pt solid windowtext;" x:str="">一台部署机(可使用node节点作为部署机)<br>安装ansible，版本建议不低于2.9<br>安装kubectl，版本建议同等与需要部署的k8s集群的版本</td>
    <td class="xl91" x:str="">非必须，通过kubectl操作需要部署的k8s集群<br>离线环境可运行centos_ansible容器用以部署服务</td>
   </tr>
   <tr height="12.40" style="height:12.40pt;">
    <td height="12.40" colspan="6" style="height:12.40pt;mso-ignore:colspan;"></td>
   </tr>
   <tr height="12.40" style="height:12.40pt;">
    <td class="xl84" height="12.40" colspan="3" style="height:12.40pt;border-right:none;border-bottom:none;" x:str="">注：除标注了【非必须】的条目，其他须由客户提供</td>
    <td colspan="3" style="mso-ignore:colspan;"></td>
   </tr>
   <tr height="12.40" style="height:12.40pt;">
    <td height="12.40" colspan="4" style="height:12.40pt;mso-ignore:colspan;"></td>
    <td class="xl92"></td>
    <td></td>
   </tr>
   <!--[if supportMisalignedColumns]-->
    <tr width="0" style="display:none;">
     <td width="100" style="width:100;"></td>
     <td width="67" style="width:67;"></td>
     <td width="133" style="width:133;"></td>
     <td width="184" style="width:184;"></td>
     <td width="166" style="width:166;"></td>
     <td width="274" style="width:274;"></td>
    </tr>
   <!--[endif]-->
  </tbody></table>