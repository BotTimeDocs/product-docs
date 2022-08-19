# 云扩控制台kubernetes私有化部署文档
# 一 .前提

根据云扩控制台kubernetes私有化部署软硬件要求文档中的内容，准备好相应资源。

## 1.1 部署机安装ansible

root用户登录到部署机，可以选择在线安装ansible或者离线环境运行ansible容器。

### 在线安装ansible

```
# centos7
yum install ansible -y

# ubuntu 18.04
apt-get install ansible -y

# 版本验证
ansible --version
```

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-1.png)

### 离线环境运行ansible容器

```
# 下载centos_ansible镜像tar包
wget "https://consolev3release.blob.core.chinacloudapi.cn/ansible/centos_ansible.tar.gz"

# 上传tar包到部署机后解压并导入镜像
tar xf centos_ansible.tar.gz 
docker load -i centos_ansible.tar

# 启动容器
docker run -d  --name centos_ansible -v /etc/ansible:/etc/ansible/ -v /root/.kube:/root/.kube -v $(which kubectl):/usr/local/bin/kubectl  encoo/centos_ansible:1.0

# 进入容器
docker exec -it centos_ansible bash
```

## 1.2 准备工作

进入ansible目录，下载或者上传控制台私有化安装包并解压，进入到控制台私有化安装包文件夹中的k8s目录

```
cd /etc/ansible
tar xf consolev4pvt-4.1.136251.tar.gz
cd consolev4pvt-4.1.136251/k8s
```

根据申请的资源填写host文件，主要填写以下内容

```
vim host

# K8s私有化部署的Namespace
NAME_SPACE=""

# 配置镜像仓库的的secret
SECRET_NAME="encoo-k8spvt-registry"
DOCKER_SERVER=""
DOCKER_USER_NAME=""
DOCKER_USER_PASSWORD="

# 域名url配置，注意访问协议确定是http还是https
# 控制台前端站点URL
CONSOLE_WEB_ENDPOINT="http://console.pvttest.com"
# 低代码前端站点URL
APPS_WEB_ENDPOINT="http://apps.pvttest.com"
# 网关站点URL
API_GATEWAY_ENDPOINT="http://gateway.pvttest.com"
# SSO站URL
AUTH_ENDPOINT="http://auth.pvttest.com"

# redis相关配置 
REDIS_OPTIONS_ENDPOINT=""
REDIS_OPTIONS_PORT="6379"
REDIS_OPTIONS_PASS=""
# True/False
REDIS_OPTIONS_SSL="False"

# mysql相关配置
MYSQL_OPTIONS_ENDPOINT=""
MYSQL_OPTIONS_PORT="3306"
MYSQL_OPTIONS_UID=""
MYSQL_OPTIONS_PWD=""
# Preferred/None
MYSQL_OPTIONS_SSLMODE="Preferred"

# oss存储配置 
OSS_TYPE="1"
# 如域名url访问协议配置为https，OBJECT_STORAGE_ENDPOINT访问协议需配置为https
OBJECT_STORAGE_ENDPOINT="http://minio-pvt.pvttest.com"
OBJECT_STORAGE_ACCESSKEY=""
OBJECT_STORAGE_SECRETKEY=""
# OBJECT_STORAGE_ENDPOINT为https，OBJECT_STORAGE_USESSL配置为true
OBJECT_STORAGE_USESSL="false"
OBJECT_STORAGE_BUCKET="pvttest"

#初始化公司信息
COMPANY_NAME="encoo"
ADMIN_USER_EMAIL="admin@pvttest.com"
ADMIN_USER_PASS="123456"
```

P.S. 根据实际情况选择是否需要配置smtp和钉钉登录。根据实际情况选择是否需要配置smtp和钉钉登录。 默认部署只生成yaml文件，后期通过kubectl手动部署服务，如需自动部署服务，则配置 IS_DEPLOY="true"。默认部署只生成yaml文件，后期通过kubectl手动部署服务，如需自动部署服务，则配置 IS_DEPLOY="true"。

host文件填写完成确认无误后依次执行操作

1.. 重命名文件后缀和占位符 重命名文件后缀和占位符

```
sh init.sh rename 
重命名文件后缀完成。
重命名文件占位符完成。
```

2.. 构建aspnet-tools镜像 构建aspnet-tools镜像

```
sh init.sh build 
构建aspnet-tools镜像完成，镜像名为 xxxxxx.harbor.com/k8spvt/aspnet-tools:4.1.136251
```

3.. 上传控制台镜像到镜像仓库 上传控制台镜像到镜像仓库

```
sh init.sh upload
push镜像完成。
```

4.. 复制部署相关文件到/etc/ansible目录 复制部署相关文件到/etc/ansible目录

```
cp -r hosts playbooks roles /etc/ansible 
```

5.. 清理无用的镜像和容器(选做) 清理无用的镜像和容器(选做)

```
docker system prune -a -f
```

### smtp服务配置

如果需要发送邮件则需要配置smtp，需要填写smtp相关配置

```
# Smtp配置
# SMTP服务器地址
SMTP_OPTIONS_HOST=""
# SMTP服务器端口
SMTP_OPTIONS_PORT=0
# SMTP发件人邮箱
SMTP_OPTIONS_SENDER_ADDRESS=""
# SMTP服务授权码
SMTP_OPTIONS_AUTHORIZATION_CODE=""
# 是否需要使用SSL加密连接
SMTP_OPTIONS_ENABLE_SSL="true"
```

### 控制台忘记密码功能

如果需要启用控制台忘记密码功能（此功能需要配置SMS服务或SMTP服务），请配置以下选项为true

```
# 配置账户选项
# 是否需要启用控制台忘记密码功能（此功能需要配置SMS服务或SMTP服务），如需启用请配置以下选项为true
ACCOUNT_OPTIONS_ALLOW_FORGET_PASSWORD=false 
ACCOUNT_OPTIONS_ALLOW_BIND_CONTACTt=false
```

### 钉钉登录配置

如果需要集成钉钉第三方登录， 则需进行额外配置相关信息

```
# 是否需要集成钉钉第三方登录
ENABLED_INTRADINGTALK="true"
# 钉钉所属组织名称 
INTRADINGTALK_COMPANYNAME=""
# 钉钉所属组织CoprId
INTRADINGTALK_CORPID=""
# 钉钉应用AppKey 
INTRADINGTALK_APPID=""
# 钉钉应用AppSecret
INTRADINGTALK_APPSECRET=""
```

# 二. 部署

准备工作完成后，在部署机上以root用户进行部署操作

进入/etc/ansible目录

```
cd  /etc/ansible 

ls
roles  ansible.cfg  hosts  playbooks ...
```

## 2.1 初始化文件和目录

执行命令

```
ansible-playbook playbooks/01.init.yml
```

当01.init.yml执行完以后应该在/etc/ansible目录下生成k8s_pvt目录，结构如下

```
k8s_pvt/
├── ssl      -- 证书目录
└── yml
    ├── base -- 基础服务yaml文件和job服务yaml文件目录
    ├── configs   -- 配置文件目录
    │   ├── console_configs
    │   ├── rpa_configs
    │   └── vicode_configs
    ├── encoo-k8spvt-registry.yaml -- 镜像仓库的secret文件，实际文件名称为host文件中的SECRET_NAME变量
    ├── idsrv4-cer.yaml  -- 证书secret文件
    └── services  -- 服务文件目录
    
```

部署encoo-k8spvt-registry.yml，idsrv4-cer.yml文件

```
# 部署docker镜像服务器secret文件，实际文件名称为host文件中的SECRET_NAME变量
kubectl apply -f k8s_pvt/yml/encoo-k8spvt-registry.yaml

# 部署identityServer秘钥secret文件
kubectl apply -f k8s_pvt/yml/idsrv4-cer.yaml
```

验证

kubectl get secrets -n 命名空间

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-2.png)

P.S. 当host文件中配置 IS_DEPLOY="true"，则执行ansible-playbook命令时自动部署yml文件，下同。当host文件中配置 IS_DEPLOY="true"，则执行ansible-playbook命令时自动部署yml文件，下同。

## 2.2  数据迁移(重要)

执行命令

```
ansible-playbook playbooks/02.migrate.yml
```

部署数据迁移yaml文件

```
# 执行foundation服务数据迁移任务
kubectl apply -f k8s_pvt/yml/base/migratev4foundationservicedata.yml
# 执行vicode服务数据迁移任务
kubectl apply -f k8s_pvt/yml/base/migratev4vicodeservicedata.yml
```

验证数据迁移完成(Completed)

kubectl get pod -n 命名空间

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-3.png)

如需重新执行某项数据迁移任务， 则需先删除之前的任务

```
# 删除foundation服务数据迁移任务
kubectl delete -f k8s_pvt/yml/base/migratev4foundationservicedata.yml
# 删除vicode服务数据迁移任务
kubectl delete -f k8s_pvt/yml/base/migratev4vicodeservicedata.yml
```

P.S. 数据库迁移必须在部署service服务之前完成。数据库迁移必须在部署service服务之前完成。

## 2.3  部署配置文件

执行命令

```
ansible-playbook playbooks/03.configs.yml 
```

部署configmap  yaml文件

```
kubectl apply -f k8s_pvt/yml/configs
```

验证

kubectl get configmaps -n 命名空间

<img width = '680'  src ="https://docimages.blob.core.chinacloudapi.cn/images/cself-1-4.png"/>

P.S. 如果对象存储使用的是阿里云oss，则修改 roles/configs/templates/console如果对象存储使用的是阿里云oss，则修改 roles/configs/templates/consoleconfigs/appsettingsconfigs/appsettingsstorage.json.j2中间的S3Type，修改为 "S3Type": "Aliyun" 后再执行ansible-playbook命令。storage.json.j2中间的S3Type，修改为 "S3Type": "Aliyun" 后再执行ansible-playbook命令。

部署configmap  yaml文件时，如遇错误The ConfigMap "console-config" is invalid: metadata.annotations: Too long: must have at most 262144 bytes，则部署命令改成 kubectl replace -f k8s_pvt/yml/configs/ --forcekubectl replace -f k8s_pvt/yml/configs/ --force

## 2.4  部署service服务

执行命令

```
ansible-playbook playbooks/04.services.yml
```

部署service yaml文件

```
kubectl apply -f k8s_pvt/yml/configs
```

部署完成， 等待命名空间下所有pod status 为 Running 并且 ready 为1/1

kubectl get pod -n 命名空间

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-5.png)

## 2.5 初始化公司及其管理员账户/上传安装包

当所有pod status 为 Running 并且 ready 为1/1后 ，执行05.initservices.yml，会在k8sservices.yml，会在k8spvt/yml/base目录下生成installeruploader.yml、organizationusercompanyinit.yml文件。pvt/yml/base目录下生成installeruploader.yml、organizationusercompanyinit.yml文件。

执行命令

```
ansible-playbook playbooks/05.init_services.yml
```

部署相关yaml文件

```
# 执行初始化公司及其管理员账户任务
kubectl apply -f k8s_pvt/yml/base/installeruploader.yml
# 执行上传安装包任务
kubectl apply -f k8s_pvt/yml/base/organizationusercompanyinit.ym
```

验证任务是否完成(Completed)

kubectl get pod -n 命名空间 | grep -E "organizationusercompanyinit|installeruploader"

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-6.png)

通过 kubectl -n 命名空间  logs organizationusercompanyinit-xxxx 查看初始化公司及其管理员账户执行结果， 如返回200/201或400则初始化成功 

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-7.png)

通过 kubectl logs  -n 命名空间 installeruploader-xxxxx | tail  查看上传安装包执行结果， 如日志最后提示为completed 上传安装包完成则上传安装包成功

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-8.png)

如需重新执行初始化公司及其管理员账户或者上传安装包任务， 则需先删除之前的任务

```
# 删除初始化公司及其管理员账户任务
kubectl delete -f k8s_pvt/yml/base/installeruploader.yml
# 删除上传安装包任务
kubectl delete -f k8s_pvt/yml/base/organizationusercompanyinit.yml
```

### 钉钉集成租户修改租户属性

当hosts文件中的变量ENABLEDINTRADINGTALK="true"， 执行05.initINTRADINGTALK="true"， 执行05.initservices.yml，会在k8s_pvt/yml/base目录下生成changecompanyproperties.yml文件services.yml，会在k8s_pvt/yml/base目录下生成changecompanyproperties.yml文件

部署changecompanyproperties.yml文件

```
# 执行修改租户属性任务，以启用钉钉组织架构同步功能
kubectl apply -f  k8s_pvt/yml/base/changecompanyproperties.yml
```

验证任务是否完成(Completed)

kubectl get pod -n 命名空间 | grep -E "organizationusercompanyinit|installeruploader"

```
kubectl get pod -n ecnoo-pvt4 | grep -E "changecompanyproperties"
输出
changecompanyproperties-w7vvf       0/1     Completed   0          3d17h
```

如需重新执行修改租户属性任务， 则需先删除之前的任务

```
# 删除修改租户属性任务
kubectl delete -f  k8s_pvt/yml/base/changecompanyproperties.yml
```

## 2.6 访问测试

部署完成，可以通过 kubectl get ingress -n 命名空间 查看部署的ingress， 确保域名正确并获取到正确的IP地址。

例如：

```
kubectl get ingress -n encoo-pvt4
NAME                           CLASS    HOSTS               ADDRESS     PORTS   AGE
console-web-v4-ingress         <none>  console.pvttest.com   IP地址       80    5d18h
apps-web-ingress               <none>  apps.pvttest.com      IP地址       80    5d18h
identity-ingress               <none>  auth.pvttest.com      IP地址       80    5d18h
apigateway-ingress             <none>  gateway.pvttest.com   IP地址       80    5d18h
apigateway-websocket-ingress   <none>  gateway.pvttest.com   IP地址       80    5d18h
```

所有域名添加记录解析， 客户端浏览器访问控制台前端站点URL
![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-9.png)

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-10.png)

部署完成后可备份部署相关文件并保存至本地

```
tar czf  k8s-consolev4pvt-4.1.136251.tar.gz hosts k8s_pvt playbooks roles
```

## 2.7 其它操作

### 2.7.1 清理

当可通过kubectl操作需要部署的k8s集群时，可执行playbooks文件夹中的99.clean.yml文件一键清理部署的服务，任务以及配置文件。

```
ansible-playbook playbooks/99.clean.yml
```

执行完成后查看k8s命名空间下pod、service、configmaps、secret、ingress、job是否被清除。

```
kubectl get -n encoo-pvt4 pod,service,configmaps,secret,ingress,job
```

## 2.8 相关问题

### 2.8.1 上传流程包出错

上传流程包出错，通过F12调试控制台显示跨域错误

Access to XMLHttpRequest at '对象存储的url地址' from origin 'xxx' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-11.png)

解决方法

对象存储配置跨域规则(一般联系客户配置)，例如

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-12.png)

### 2.8.2 新建连接管理显示异常

数据中心->连接管理->新建 显示异常

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-13.png)

或者 文件服务->新建文件夹->绑定连接器-新建文件类连接 显示异常

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-14.png)

解决方法

删除dataentity服务pod后让其重新生成pod

kubectl get pod -n 命名空间 | grep dataentity kubectl delete pod  -n 命名空间  pod名称kubectl delete pod  -n 命名空间  pod名称

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-15.png)

验证

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-16.png)

![](https://docimages.blob.core.chinacloudapi.cn/images/cself-1-17.png)

# 三. 升级

1.. 在部署机上清理之前的相关部署文件和目录，保留/etc/ansible/k8s_pvt/ssl目录 在部署机上清理之前的相关部署文件和目录，保留/etc/ansible/k8s_pvt/ssl目录

```
# 创建备份目录
mkdir /tmp/pvtbackup$(date +%F)
# 移动之前的相关部署文件和目录到备份目录(备份目录名称以实际为准)
cd  /etc/ansible
mv playbooks roles hosts /tmp/pvtbackupxxxx-xx-xx
mv k8s_pvt/yml /tmp/pvtbackupxxxx-xx-xx
```

P.S. 升级需保留/etc/ansible/k8s_pvt/ssl目录升级需保留/etc/ansible/k8s_pvt/ssl目录

/etc/ansible/目录下如果存在k8spvtpvtv4目录，请重命名为k8s_pvt目录v4目录，请重命名为k8s_pvt目录 mv /etc/ansible/k8smv /etc/ansible/k8spvtpvtv4  /etc/ansible/k8s_pvtv4  /etc/ansible/k8s_pvt

2.. 执行准备工作 执行准备工作

P.S. hosts文件中相关内容如无更改，需沿用之前部署时填写的内容。hosts文件中相关内容如无更改，需沿用之前部署时填写的内容。

3.. 依次执行部署步骤2.1-2.4，注意数据库迁移必须在部署service服务之前完成 依次执行部署步骤2.1-2.4，注意数据库迁移必须在部署service服务之前完成

P.S. 执行2.1的时候k8s_pvt/yml目录下不会生成idsrv4-cer.yml文件，所以也无需部署identityServer秘钥secret文件， 只需部署docker镜像服务器secret文件执行2.1的时候k8s_pvt/yml目录下不会生成idsrv4-cer.yml文件，所以也无需部署identityServer秘钥secret文件， 只需部署docker镜像服务器secret文件

4.. 跳过2.5中的初始化公司及其管理员账户任务，执行上传安装包任务 跳过2.5中的初始化公司及其管理员账户任务，执行上传安装包任务 55.. 访问测试 访问测试

# 四. kubectl常用命令

```
# 查看各类资源
kubectl get -n <namespace> pod|deployments|statefulset|configmaps|secrets|ingress 

# 查看具体某个资源的yaml文件，以pod为例
kubectl get -n <namespace> pod  <podname> -oyaml

# 部署yaml文件
kubectl apply -f <filename>|<dirname>
kubectl replace -f <filename>|<dirname>

# 获取pod详细信息
kubectl -n <namespace> describe pod <podname>

# 获取pod日志
kubectl -n <namespace> logs [-f] [-p] [-c containername] <podname> 

#进入容器
kubectl -n <namespace> exec -it <podname> [-c containername] bash

# 复制容器内/tmp/foo文件到本地
kubectl cp -c <containername> <some-namespace>/<some-pod>:/tmp/foo /tmp/bar

# 打印客户端和服务版本信息
kubectl version
```