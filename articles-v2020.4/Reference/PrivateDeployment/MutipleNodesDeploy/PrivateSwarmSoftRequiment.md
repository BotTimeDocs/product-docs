# 云扩控制台swarm私有化部署软硬件要求

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-q3we{background-color:#FF0;color:#F00;text-align:left;vertical-align:middle}
.tg .tg-1p3a{background-color:#9BC2E6;font-weight:bold;text-align:left;vertical-align:middle}
.tg .tg-7zrl{text-align:left;vertical-align:bottom}
.tg .tg-027g{background-color:#9BC2E6;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
.tg .tg-0lax{text-align:left;vertical-align:top}
.tg .tg-p8v2{background-color:#FF0;color:#F00;text-align:center;vertical-align:bottom}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 634px">
<colgroup>
<col style="width: 116px">
<col style="width: 68px">
<col style="width: 85px">
<col style="width: 129px">
<col style="width: 105px">
<col style="width: 131px">
</colgroup>
<thead>
  <tr>
    <th class="tg-1p3a"></th>
    <th class="tg-cly1" colspan="2"></th>
    <th class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">推荐配置</span></th>
    <th class="tg-7zrl"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">备注</span></th>
    <th class="tg-7zrl"></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-027g" rowspan="11"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">控制台</span></td>
    <td class="tg-nrix" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">硬件要求</span><br><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">（高可用方案最低3台服务器节点）</span></td>
    <td class="tg-cly1" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">4 CPU</span><br><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">8 GB 内存</span><br><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">100 GB 空闲磁盘</span></td>
    <td class="tg-7zrl"></td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="10"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">软件要求</span></td>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">操作系统</span></td>
    <td class="tg-cly1" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">CentOS 7.4及以上或linux内核版本在4.0以上的Linux发行版</span></td>
    <td class="tg-7zrl"></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">端口开放</span></td>
    <td class="tg-cly1" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">控制台前端站点 console-web-v4， 默认端口 80低代前端站点 apps-web，默认端口 82单点登录站点 identity-service，默认端口 81接口网关站点 apigateway-service，默认端口 8080对象存储服务 默认端口9000Swarm集群之间通信端口： 2377 7946 4789</span></td>
    <td class="tg-7zrl"></td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="3"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">访问入口负载均衡</span></td>
    <td class="tg-0lax" colspan="2" rowspan="3"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1.域名访问；2. 域名+端口访问；3.IP+端口访问； （以上三种访问方式，都需要配置好转发策略）（第一种域名访问方式，需要申请五个一级域名（控制台前端服务，授权认证服务，对象存储服务；API网关接入服务，小程序web前端服务）（第二种访问方式，至少需要申请一个域名）</span></td>
    <td class="tg-7zrl" rowspan="3"></td>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">NFS服务</span></td>
    <td class="tg-cly1" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">集群节点挂载NFS服务共享目录，共享部署文件</span></td>
    <td class="tg-nrix"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">非必须，用于提供统一的部署文件和日志存储</span></td>
  </tr>
  <tr>
    <td class="tg-q3we"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">对象存储服务</span></td>
    <td class="tg-cly1" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">兼容S3接口的对象储存（需要配置跨域策略）</span></td>
    <td class="tg-7zrl"></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">mysql服务</span></td>
    <td class="tg-cly1" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Mysql 5.7及以上版本</span></td>
    <td class="tg-7zrl"></td>
  </tr>
  <tr>
    <td class="tg-cly1"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">redis服务</span></td>
    <td class="tg-cly1" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Redis4.x及以上版本</span></td>
    <td class="tg-7zrl"></td>
  </tr>
  <tr>
    <td class="tg-7zrl"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">容器注册表</span></td>
    <td class="tg-7zrl" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">上传镜像到容器注册表，供服务器下载控制台镜像</span></td>
    <td class="tg-7zrl"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">非必须，用于提供镜像存储服务</span></td>
  </tr>
  <tr>
    <td class="tg-p8v2" colspan="4"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#F00;background-color:#FF0">注：除标注了【非必须】的条目，其他须由客户提</span></td>
    <td class="tg-7zrl"></td>
    <td class="tg-7zrl"></td>
  </tr>
</tbody>
</table>