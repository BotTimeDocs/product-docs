# 云扩控制台kubernetes私有化部署软硬件要求

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-027g{background-color:#9BC2E6;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
.tg .tg-7zrl{text-align:left;vertical-align:bottom}
.tg .tg-p8v2{background-color:#FF0;color:#F00;text-align:center;vertical-align:bottom}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 693px">
<colgroup>
<col style="width: 104px">
<col style="width: 61px">
<col style="width: 76px">
<col style="width: 116px">
<col style="width: 143px">
<col style="width: 193px">
</colgroup>
<thead>
  <tr>
    <th class="tg-027g" rowspan="8">控制台 Console<br>（含ViCode）</th>
    <th class="tg-nrix" colspan="2">硬件要求<br>（K8S高可用方案<br>最低3台node节点）<br></th>
    <th class="tg-cly1">8核 CPU<br>16GB 内存<br>100GB 空闲磁盘</th>
    <th class="tg-cly1">16核 CPU或更高<br>32GB 内存或更高<br>100GB 以上空闲磁盘</th>
    <th class="tg-7zrl"></th>
  </tr>
  <tr>
    <th class="tg-nrix" rowspan="7">软件<br>要求</th>
    <th class="tg-cly1">K8S命名空间</th>
    <th class="tg-cly1" colspan="2">一个独立的命名空间</th>
    <th class="tg-cly1">如果命名空间使用了LimitRange，limits每个pod至少为0.5core 2G<br><br>如果命名空间使用ResourceQuota， 命名空间ResourceQuota配额request/limits总额至少不低于控制台所有pod的request/limits总和</th>
  </tr>
  <tr>
    <th class="tg-cly1">对象存储服务</th>
    <th class="tg-cly1" colspan="2">兼容S3接口的对象储存（需要配置跨域策略）</th>
    <th class="tg-7zrl"></th>
  </tr>
  <tr>
    <th class="tg-cly1">mysql服务</th>
    <th class="tg-cly1" colspan="2">Mysql 5.7及以上版本</th>
    <th class="tg-7zrl"></th>
  </tr>
  <tr>
    <th class="tg-cly1">redis服务</th>
    <th class="tg-cly1" colspan="2">Redis4.x及以上版本</th>
    <th class="tg-7zrl">支持单机/主从/哨兵模式，不支持集群模式。</th>
  </tr>
  <tr>
    <th class="tg-cly1">镜像存储服务</th>
    <th class="tg-cly1" colspan="2">例如harbor，ACR等</th>
    <th class="tg-7zrl">上传控制台镜像到镜像仓库，供kubernetes下载</th>
  </tr>
  <tr>
    <th class="tg-cly1">访问方式</th>
    <th class="tg-cly1" colspan="2">通过ingress暴露服务(ingress-nginx)  <br><br>浏览器通过域名访问控制台，需要申请四个域名<br>1.控制台前端站点域名 2.低代前端站点域名<br>3.单点登录站点域名 4.接口网关站点域名<br><br>确定访问协议是http还是https</th>
    <th class="tg-cly1">云扩RPA控制台相关的服务均承载在K8S集群中，服务通过ingress将内部服务暴露出来供外部访问</th>
  </tr>
  <tr>
    <th class="tg-cly1">其它要求</th>
    <th class="tg-cly1" colspan="2">一台部署机(可使用node节点作为部署机)<br>安装ansible，版本建议不低于2.9<br>安装kubectl，版本建议同等与需要部署的k8s集群的版本</th>
    <th class="tg-cly1">非必须，通过kubectl操作需要部署的k8s集群<br>离线环境可运行centos_ansible容器用以部署服务</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-p8v2" colspan="6">注：除标注了【非必须】的条目，其他须由客户提供</td>
  </tr>
</tbody>
</table>