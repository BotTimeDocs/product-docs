# 企业级运维

## 私有化部署指南

### 为什么需要私有化部署
客户一般出于数据安全或网络隔离等场景，会有控制台私有化部署的需求。

#### 环境需求
不同的部署方案，软硬件要求各有区别。控制台当前支持三种私有化部署方式，均为容器化部署，各自环境详情见文档。

- 单机部署
    单机部署方案仅需单台Linxu机器即可部署，采用Docker Compose在单台机器上部署控制台服务，自带控制台依赖的数据库，缓存，对象存储等（支持配置使用外部数据库等)。
    > **说明：**
    > 如下表格中，除标注【非必须】的条目，其他须由客户提供。

    ![控制台配置](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console-one.png)

- Docker Swarm多节点部署
    多节点部署方案最少需要三台机器组成Docker Swarm集群，控制台相关服务以容器化的方式部署于三节点Swarm集群中。
    > **说明：**
    > 此种部署方案，需要客户额外提供Mysql，Redis以及兼容S3接口的对象存储服务。

    ![控制台配置](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console-swarm1.png)

- k8s部署
    k8s部署方案适用于客户已存在k8s基础平台的场景，集群需具备通过ingress暴露服务的能力。
    > **说明：**
    > 云扩不提供k8s集群的搭建和运维。与多节点部署类似，此种部署方案，需要客户额外提供Mysql，Redis以及兼容S3接口的对象存储服务。

    ![控制台配置](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console-K8S.png)



### 高可用指南

#### 私有化控制台Docker Swarm高可用版部署

##### 概况


- 机器：10.10.10.1, 10.10.10.2, 10.10.10.3 三台服务器
- 外部负载均衡器（F5或其他IP负载均衡）
- 控制台私有化安装包
- Redis4.x及以上版本
- Mysql5.7及以上版本
- S3接口对象存储
- 安装
    1. 以下为模拟流程提供如下三台服务器: </br>
    CentosA: 10.10.10.1 </br>
    CentosB: 10.10.10.2 </br>
    CentosC: 10.10.10.3 </br>
    2. 云扩控制台安装包：consolev4pvt-4.1.141211
    3. Docker离线安装 </br>
    安装方式：二进制安装 </br>
    版本：19.03.13 </br>
    安装文件：[docker-19.03.13.tgz]、[docker.service]、[docker.socket] </br>
    docker安装文件下载：https://pan.baidu.com/s/106Rw-ZWSMTrEWGtTS-ymAQ </br>
    提取码：5ct3 </br>
    4. 操作用户：root </br>
    在CentosA,CentosB,CentosC 三台服务器上进行相同的操作，上传私有化控制台安装包，docker安装文件到服务器指定目录 /app 目录（也可自定义目录）；执行安装docker服务的命令。
```` 
    # 创建一个统一存放安装控制台的目录
    cd  /
    make  -p  app
    #进入到该目录，把docker安装文件，控制台安装包通过sftp上传到该目录下面
    #查看服务器防火墙状态，
    systemctl status firewalld
    #如果防火墙状态是running,开启的状态，执行命令，关闭防火墙
    systemctl stop firewalld
    #进入到app目录，安装docker服务
    cd  /app
    tar xf docker-19.03.13.tgz
    cp docker/*  /usr/bin/
    cp docker.socket  /etc/systemd/system/
    cp docker.service  /etc/systemd/system/
    systemctl daemon-reload
    systemctl start docker.service
    systemctl enable docker.service
    systemctl status docker.service
    #退出该状态
    Ctrl+c
````
##### Swarm 集群的搭建
操作用户：root

1. CentosA服务器中进行以下操作，执行Swarm集群初始化的命令
````
#进入到app目录下面
cd  /app
# swarm集群初始化，创建Swarm集群
docker swarm init
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console53.png)

2. CentosB,CentosC 服务器中执行以下相同操作，执行节点加入Swarm集群的命令
````
#进入到app目录
cd  /app
#执行如下命令，加入到Swarm集群中，以下命令取自上一步执行结果的内容
docker swarm join --token SWMTKN-1-3qe4y4fz7wyhk6rzkbn3sdsx297ck7lrg0lxt3iqsdoh5y4zz1-0bgesujg10h2tpfzn5kxf69yp 172.18.0.16:2377
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console54.png)


3. CentosA 服务器上进入以下操作，查看Swarm 集群状态，执行集群节点加入管理集群节点的命令
````
#进入到app目录下面
cd  /app
#查看Swarm集群状态
docker  node  ls
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console06.png)

````
#设置集群管理节点，节点id取自上一步操作执行结果的id
  docker  node  promote  mdvemqwhj9sj04w0zmazans7i
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console07.png)

````
docker  node  promote  6uxufag8ihz9fx86bwl35zf6f
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console08.png)

````
#设置完成后，类似于如下图  
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console09.png)



##### 控制台的部署

###### CentosA,CentosB,CentosC,三台服务器上进行以下相同的操作，执行加载镜像文件的命令
````
#进入到app目录
cd  /app 
#解压控制台压缩包consolev4pvt-4.1.141211
 tar  -zxvf  consolev4pvt-4.1.141211.tar.gz
#进入到控制台执行目录
 cd consolev4pvt-4.1.141211/swarm
#加载镜像
  sh  ha-deploy.sh  update
````

###### CentosA 服务器上进行以下操作，执行控制台初始化

根据Swarm高可用部署选择的访问负载均衡方式，初始化控制台访问域名部分的填写可以分为以下三种: </br>
访问负载均衡方式的控制台目前有三种：1.多域名；2.域名+端口; 3.IP+端口 

> **说明：**
> 1，以上三种访问方式，都需要在负载均衡中配置好转发策略;
> 2，控制台前端服务，授权认证服务，对象存储服务，API网关接入服务，小程序web前端服务;
> 3，第一种域名访问方式，需要申请五个域名;
> 4，第二种域名+端口的访问 方式，至少需要申请一个域名;
> 5，实际域名和访问IP以客户提供为准，以下域名和IP都是举例;



**控制台的初始化操作根据客户提供的资源，进行初始化操作：** </br>
客户提供的资源： </br>
1. Mysql5.7及以上版本（必要）
2. Redis4.x及以上版本（可选）
3. S3存储 （可选）(不能提供S3存储服务，需要提供NFS文件共享服务)
4. 访问方式为http的请求，执行控制台初始化操作
举例如下: </br>
- 第一种多域名访问 </br>
**域名:** </br>
www.consoleweb.com </br>
www.appsweb.com </br>
www.apigateway.com </br>
www.sso.com </br>
www.s3storage.com </br>
**服务访问地址:** </br>
www.consoleweb.com (控制台前端服务域名); </br>
www.appsweb.com (小程序web前端服务域名);  </br>
www.apigateway.com (API网关接入服务域名);  </br>
www.sso.com (授权认证服务域名); </br>
www.s3storage.com (S3对象储存服务域名) </br>
````
#控制台初始化， 
sh  ha-deploy.sh  init
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console10.png)
> **说明：**
> 1，注释:红框内容是根据客户提供的资源，选项存储对象和redis信息,此处是客户提供redis和存储服务; 是否填写外部对象存储和Redis，选择”Y”或者”N”以客户提供的资源为主)。

- 第二种(域名+端口)访问 </br>
**域名:** </br>
www.rpadomain.com </br>
**默认端口:** </br>
consolewebport>80 </br>
ssoport>81 </br>
appswebport>82 </br>
apigatewayport>8080 </br>
s3storageport> 需要跟客户确认对方提供的存储服务端口$port(此处以9000端口举例) </br>
**服务访问地址:** </br>
www.rpadomain.com (控制台前端服务域名);  </br>
www.rpadomain.com:82 (小程序web前端服务域名);  </br>
www.rpadomain.com:8080 (API网关接入服务域名); </br>
www.rpadomain.com:81 (授权认证服务域名); </br>
www.rpadomain.com:$port (S3对象储存服务域名) </br>
````
#控制台初始化
sh ha-deploy.sh init
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console11.png)
> **说明：**
> 1，注释:红框内容是根据客户提供的资源进行的选择，此处选择操作，客户提供了Redis，因为没有提供对象存储服务，使用的是安装包自带的Minio存储服务，所以客户要提供NFS文件共享服务；是否填写外部对象存储和Redis，选择”Y”或者”N”以客户提供的资源为主)。

- 第三种(IP+端口)访问 </br>
**负载均衡IP地址：** </br>
52.131.87.118 </br>
**默认端口：** </br>
consolewebport>80 </br>
ssoport>81 </br>
appswebport>82 </br>
apigatewayport>8080 </br>
s3storageport>需要跟客户确认提供的存储服务的端口$port  </br>
**服务访问地址**  </br>
52.131.87.118 (控制台前端服务访问地址);  </br>
52.131.87.118:82 (小程序web前端服务访问地址);  </br>
52.131.87.118.82:8080 (API网关接入服务地址); </br>
52.131.87.118:81 (授权认证服务访问地址); </br>
52.131.87.118:$prot (S3对象存储服务访问地址。此次以9000端口举例)

````
#初始化控制台
sh ha-deploy.sh init
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console12.png)
> **说明：**
> 1，注释:红框内容是根据客户提供的资源进行的选择，此处选择操作，客户没有提供Redis和对象存储，Redis和对象存储使用的私有化安装包自带的。因为没有提供对象存储服务，使用的是安装包自带的Minio存储服务，所以客户要提供NFS文件共享服务；是否填写外部对象存储和Redis，选择”Y”或者”N”以客户提供的资源为主。

**查看初始化完成后的信息**
````
#在执行初始化当前的目录，查看初始化完成后生成的信息（看下面红框的内容） 
cat .userconfig
````
- IP+端口访问方式：
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console15.png)

- 多域名访问方式：
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console16.png)

- 单域名访问方式：
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console17.png)
> **说明：**
> 1，注释:红框内容就是生成的访问各种服务的URL地址，实际地址以客户提供为准


###### CentosA 服务器上进行以下操作，执行控制台的部署命令
````
#执行部署服务操作
sh ha-deploy.sh start
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console18.png)


###### 公司初始化，上传安装包命令操作
````
#查看服务是否全部启动，
docker service ls
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console19.png)
> **说明：**
> 1，注释：上图中 REPLICAS 列对应的副本数，斜杠左右两边数字一致，表明服务已全部启动)

````
#等服务全部启动成功之后，才能进行公司初始化操作命令
sh ha-deploy.sh organizationUserCompanyInit
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console20.png)

````
#执行上传安装包操作命令
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console21.png)


##### Swarm 高可用验证
CentosA 服务器上进行以下操作，执行查看服务状态的命令
````
#进入到app目录
cd  /app
# 查看Swarm服务状态
docker  service  ls
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console22.png)

> **说明：**
> 1，REPLICAS 对应列，左右边的数值都保持相同了，说明服务已全部启动。

##### 客户端浏览器访问控制台
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console23.png)

在浏览器中输入登录地址
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console24.png)


##### 高可用控制台的升级

###### CentosA 服务器上进行以下操作，停止服务
````
#进入到app目录
cd  /app 
#进入到控制台的执行目录
cd consolev4pvt-4.0.113501/swarm
#停止服务操作
sh ha-deploy.sh stop
````

###### 在CentosA,CentosB,CentosC 三台服务器上进行相同的操作，上传最新私有化控制台安装包到/app目录(也可自定义目录),解压
````
#进入到app目录
cd /app
#解压新上传的私有化控制台安装包
tar -zxvf consolev4pvt-4.1.118041.tar.gz
````

###### 在CentosA,CentosB,CentosC 三台服务器上进行相同的操作,加载镜像
````
#进入到控制台目录
cd consolev4pvt-4.1.118041/swarm/
#进行加载镜像操作
sh ha-deploy.sh update
````

###### CentosA 服务器上进行控制台初始化操作
````
#进入到控制台目录
cd  /app/ consolev4pvt-4.1.118041/swarm
#原有控制台初始化操作，是按照init 参数，现在的控制台就按照以下操作命令进行
sh ha-deploy.sh init
#原有控制台初始化操作，是按照initmore参数，现在的控制台就按照以下操作命令进行
sh ha-deploy.sh initmore
````

###### CentosA 服务器上进行数据迁移操作
````
#进入到控制台目录
cd  /app/ consolev4pvt-4.1.118041/swarm
#执行数据迁移操作
sh ha-deploy.sh dataMigrationFoundation
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console25.png)

````
sh ha-deploy.sh dataMigrationVicode
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console26.png)

###### CentosA 服务器上进行启动控制台服务操作
````
#进入到控制台目录
cd  /app/ consolev4pvt-4.1.118041/swarm
#控制台开始部署,执行部署命令操作
sh ha-deploy.sh start
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console27.png)

###### 公司初始化，上传安装包命令操作
````
#查看服务是否全部启动，
docker service ls
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console28.png)
> **说明：**
> 1，上图中 REPLICAS 列对应的副本数，斜杠左右两边数字一致，表明服务已全部启动

````
#等服务全部启动成功之后，才能进行公司初始化操作命令
sh ha-deploy.sh organizationUserCompanyInit
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console29.png)

````
#执行上传安装包操作命令
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console30.png)


###### 客户端浏览器访问控制台
````
#打开浏览器输入登录地址
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console31.png)
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console32.png)

##### 常规需求

###### 部署控制台非root 账号部署方案解决
创建的appuser普通用户加入docker组
操作用户：root
在CentosA,CentosB,CentosC 三台服务器上执行以下相同的操作，执行非root账户加入docker组的命令

````
groupadd  docker
gpasswd  -a  rpauser   docker
systemctl  restart docker
chmod  a+rw  /var/run/ docker.sock
#操作完成之后，就可以切换到普通用户进行控制台的部署
````

###### 服务器文件根目录空间不够用
docker根目录修改
操作用户：root
在CentosA,CentosaB,CentosC 三台服务器上进行以下相同的操作，执行转移docker根目录的命令

````
#进入到app目录下面，创建docker目录
make -p  Dockerdir
# 查询 docker服务所在位置
docker info |grep “Dodcker Root Dir”
例如docker所在目录 
 /var/lib/docker
#停止docker 服务
systemctl stop docker.service
#移动到指定目录文件中   /app/Dockerdir
mv  /var/lib/docker/   /app/Dockerdir/
#创建软连接
ln -s  /app/Dockerdir/docker/   /var/lib
#重新启动docker服务
systemctl  start  docker.service
````

#### 云扩控制台kubernetes私有化部署

##### 前提
根据云扩控制台kubernetes私有化部署软硬件要求文档中的内容，准备好相应资源。

###### 部署机安装ansible
root用户登录到部署机，可以选择在线安装ansible或者离线环境运行ansible容器。

**在线安装ansible：**
````
# centos7
yum install ansible -y

# ubuntu 18.04
apt-get install ansible -y

# 版本验证
ansible --version
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console33.png)


**离线环境运行ansible容器**
````
# 下载centos_ansible镜像tar包
wget "https://consolev3release.blob.core.chinacloudapi.cn/ansible/centos_ansible.tar.gz"

# 上传tar包到部署机后解压并导入镜像
tar xf centos_ansible.tar.gz 
docker load -i centos_ansible.tar

# 启动容器
docker run -d  --name centos_ansible -v /etc/ansible:/etc/ansible/ -v /root/.kube:/root/.kube -v $(which kubectl):/usr/local/bin/kubectl  encoo/centos_ansible:1.0

# 进入容器
docker exec -it centos_ansible bash
````

###### 准备工作
进入ansible目录，下载或者上传控制台私有化安装包并解压，进入到控制台私有化安装包文件夹中的k8s目录：
````
cd /etc/ansible
tar xf consolev4pvt-4.1.136251.tar.gz
cd consolev4pvt-4.1.136251/k8s
````

根据申请的资源填写host文件，主要填写以下内容：
````
vim host

# K8s私有化部署的Namespace
NAME_SPACE=""

# 配置镜像仓库的的secret
SECRET_NAME="encoo-k8spvt-registry"
DOCKER_SERVER=""
DOCKER_USER_NAME=""
DOCKER_USER_PASSWORD="

# 域名url配置，注意访问协议确定是http还是https
# 控制台前端站点URL
CONSOLE_WEB_ENDPOINT="http://console.pvttest.com"
# 低代码前端站点URL
APPS_WEB_ENDPOINT="http://apps.pvttest.com"
# 网关站点URL
API_GATEWAY_ENDPOINT="http://gateway.pvttest.com"
# SSO站URL
AUTH_ENDPOINT="http://auth.pvttest.com"

# redis相关配置 
REDIS_OPTIONS_ENDPOINT=""
REDIS_OPTIONS_PORT="6379"
REDIS_OPTIONS_PASS=""
# True/False
REDIS_OPTIONS_SSL="False"

# mysql相关配置
MYSQL_OPTIONS_ENDPOINT=""
MYSQL_OPTIONS_PORT="3306"
MYSQL_OPTIONS_UID=""
MYSQL_OPTIONS_PWD=""
# Preferred/None
MYSQL_OPTIONS_SSLMODE="Preferred"

# oss存储配置 
OSS_TYPE="1"
# 如域名url访问协议配置为https，OBJECT_STORAGE_ENDPOINT访问协议需配置为https
OBJECT_STORAGE_ENDPOINT="http://minio-pvt.pvttest.com"
OBJECT_STORAGE_ACCESSKEY=""
OBJECT_STORAGE_SECRETKEY=""
# OBJECT_STORAGE_ENDPOINT为https，OBJECT_STORAGE_USESSL配置为true
OBJECT_STORAGE_USESSL="false"
OBJECT_STORAGE_BUCKET="pvttest"

#初始化公司信息
COMPANY_NAME="encoo"
ADMIN_USER_EMAIL="admin@pvttest.com"
ADMIN_USER_PASS="123456"
````

> **说明：**
> 1，根据实际情况选择是否需要配置smtp和钉钉登录。根据实际情况选择是否需要配置smtp和钉钉登录。
> 2，默认部署只生成yaml文件，后期通过kubectl手动部署服务，如需自动部署服务，则配置 IS_DEPLOY="true"。默认部署只生成yaml文件，后期通过kubectl手动部署服务，如需自动部署服务，则配置 IS_DEPLOY="true"。

host文件填写完成确认无误后依次执行操作:
1. 重命名文件后缀和占位符 重命名文件后缀和占位符
````
sh init.sh rename 
重命名文件后缀完成。
重命名文件占位符完成。
````

2. 构建aspnet-tools镜像 构建aspnet-tools镜像
````
sh init.sh build 
构建aspnet-tools镜像完成，镜像名为 xxxxxx.harbor.com/k8spvt/aspnet-tools:4.1.136251
````

3. 上传控制台镜像到镜像仓库 上传控制台镜像到镜像仓库
````
sh init.sh upload
push镜像完成。
````

4. 复制部署相关文件到/etc/ansible目录 复制部署相关文件到/etc/ansible目录
````
cp -r hosts playbooks roles /etc/ansible 
````

5. 清理无用的镜像和容器(选做) 清理无用的镜像和容器(选做)
````
docker system prune -a -f
````

**smtp服务配置**
如果需要发送邮件则需要配置smtp，需要填写smtp相关配置
````
# Smtp配置
# SMTP服务器地址
SMTP_OPTIONS_HOST=""
# SMTP服务器端口
SMTP_OPTIONS_PORT=0
# SMTP发件人邮箱
SMTP_OPTIONS_SENDER_ADDRESS=""
# SMTP服务授权码
SMTP_OPTIONS_AUTHORIZATION_CODE=""
# 是否需要使用SSL加密连接
SMTP_OPTIONS_ENABLE_SSL="true"
````

**控制台忘记密码功能**
如果需要启用控制台忘记密码功能（此功能需要配置SMS服务或SMTP服务），请配置以下选项为true。
````
# 配置账户选项
# 是否需要启用控制台忘记密码功能（此功能需要配置SMS服务或SMTP服务），如需启用请配置以下选项为true
ACCOUNT_OPTIONS_ALLOW_FORGET_PASSWORD=false 
ACCOUNT_OPTIONS_ALLOW_BIND_CONTACTt=false
````

**钉钉登录配置**
如果需要集成钉钉第三方登录， 则需进行额外配置相关信息。
````
# 是否需要集成钉钉第三方登录
ENABLED_INTRADINGTALK="true"
# 钉钉所属组织名称 
INTRADINGTALK_COMPANYNAME=""
# 钉钉所属组织CoprId
INTRADINGTALK_CORPID=""
# 钉钉应用AppKey 
INTRADINGTALK_APPID=""
# 钉钉应用AppSecret
INTRADINGTALK_APPSECRET=""
````

##### 部署
准备工作完成后，在部署机上以root用户进行部署操作，进入/etc/ansible目录。
````
cd  /etc/ansible 

ls
roles  ansible.cfg  hosts  playbooks ...
````

###### 初始化文件和目录
执行命令：
````
ansible-playbook playbooks/01.init.yml
````

当01.init.yml执行完以后应该在/etc/ansible目录下生成k8s_pvt目录，结构如下：
````
k8s_pvt/
├── ssl      -- 证书目录
└── yml
    ├── base -- 基础服务yaml文件和job服务yaml文件目录
    ├── configs   -- 配置文件目录
    │   ├── console_configs
    │   ├── rpa_configs
    │   └── vicode_configs
    ├── encoo-k8spvt-registry.yaml -- 镜像仓库的secret文件，实际文件名称为host文件中的SECRET_NAME变量
    ├── idsrv4-cer.yaml  -- 证书secret文件
    └── services  -- 服务文件目录
    
````

部署encoo-k8spvt-registry.yml，idsrv4-cer.yml文件：
````
# 部署docker镜像服务器secret文件，实际文件名称为host文件中的SECRET_NAME变量
kubectl apply -f k8s_pvt/yml/encoo-k8spvt-registry.yaml

# 部署identityServer秘钥secret文件
kubectl apply -f k8s_pvt/yml/idsrv4-cer.yaml
````

验证： </br>
kubectl get secrets -n 命名空间 </br>
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console34.png)

> **说明：**
> 1，当host文件中配置 IS_DEPLOY="true"，则执行ansible-playbook命令时自动部署yml文件，下同。
> 2，当host文件中配置 IS_DEPLOY="true"，则执行ansible-playbook命令时自动部署yml文件，下同。

###### 数据迁移(重要)
执行命令：
````
ansible-playbook playbooks/02.migrate.yml
````
部署数据迁移yaml文件：
````
# 执行foundation服务数据迁移任务
kubectl apply -f k8s_pvt/yml/base/migratev4foundationservicedata.yml
# 执行vicode服务数据迁移任务
kubectl apply -f k8s_pvt/yml/base/migratev4vicodeservicedata.yml
````

验证数据迁移完成(Completed) </br>
kubectl get pod -n 命名空间 </br>
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console35.png)


如需重新执行某项数据迁移任务， 则需先删除之前的任务：
````
# 删除foundation服务数据迁移任务
kubectl delete -f k8s_pvt/yml/base/migratev4foundationservicedata.yml
# 删除vicode服务数据迁移任务
kubectl delete -f k8s_pvt/yml/base/migratev4vicodeservicedata.yml
````

> **说明：**
> 1，数据库迁移必须在部署service服务之前完成。数据库迁移必须在部署service服务之前完成。

###### 部署配置文件

执行命令：
````
ansible-playbook playbooks/03.configs.yml 
````

部署configmap  yaml文件：
````
kubectl apply -f k8s_pvt/yml/configs
````

验证 </br>
kubectl get configmaps -n 命名空间 </br>
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console36.png)

> **说明：**
> 1，如果对象存储使用的是阿里云oss，则修改 roles/configs/templates/console如果对象存储使用的是阿里云oss，则修改 roles/configs/templates/consoleconfigs/appsettingsconfigs/appsettingsstorage.json.j2中间的S3Type，修改为 "S3Type": "Aliyun" 后再执行ansible-playbook命令。storage.json.j2中间的S3Type，修改为 "S3Type": "Aliyun" 后再执行ansible-playbook命令。
> 部署configmap  yaml文件时，如遇错误The ConfigMap "console-config" is invalid: metadata.annotations: Too long: must have at most 262144 bytes，则部署命令改成:
> kubectl replace -f k8s_pvt/yml/configs/ --forcekubectl replace -f k8s_pvt/yml/configs/ --force


###### 部署service服务
执行命令:
````
ansible-playbook playbooks/04.services.yml
````

部署service yaml文件
````
kubectl apply -f k8s_pvt/yml/configs
````

部署完成， 等待命名空间下所有pod status 为 Running 并且 ready 为1/1
kubectl get pod -n 命名空间
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console37.png)

###### 初始化公司及其管理员账户/上传安装包

当所有pod status 为 Running 并且 ready 为1/1后 ，执行05.initservices.yml，会在k8sservices.yml，会在k8spvt/yml/base目录下生成installeruploader.yml、organizationusercompanyinit.yml文件。pvt/yml/base目录下生成installeruploader.yml、organizationusercompanyinit.yml文件。
执行命令:
````
ansible-playbook playbooks/05.init_services.yml
````

部署相关yaml文件
````
# 执行初始化公司及其管理员账户任务
kubectl apply -f k8s_pvt/yml/base/installeruploader.yml
# 执行上传安装包任务
kubectl apply -f k8s_pvt/yml/base/organizationusercompanyinit.ym
````

验证任务是否完成(Completed) </br>
````
kubectl get pod -n 命名空间 | grep -E "organizationusercompanyinit|installeruploader"
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console38.png)

通过 kubectl -n 命名空间  logs organizationusercompanyinit-xxxx 查看初始化公司及其管理员账户执行结果， 如返回200/201或400则初始化成功 
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console39.png)

通过 kubectl logs  -n 命名空间 installeruploader-xxxxx | tail  查看上传安装包执行结果， 如日志最后提示为completed 上传安装包完成则上传安装包成功
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console40.png)

如需重新执行初始化公司及其管理员账户或者上传安装包任务， 则需先删除之前的任务
````
# 删除初始化公司及其管理员账户任务
kubectl delete -f k8s_pvt/yml/base/installeruploader.yml
# 删除上传安装包任务
kubectl delete -f k8s_pvt/yml/base/organizationusercompanyinit.yml
````

**钉钉集成租户修改租户属性** </br>
当hosts文件中的变量ENABLEDINTRADINGTALK="true"， 执行05.initINTRADINGTALK="true"， 执行05.initservices.yml，会在k8s_pvt/yml/base目录下生成changecompanyproperties.yml文件services.yml，会在k8s_pvt/yml/base目录下生成changecompanyproperties.yml文件
部署changecompanyproperties.yml文件
````
# 执行修改租户属性任务，以启用钉钉组织架构同步功能
kubectl apply -f  k8s_pvt/yml/base/changecompanyproperties.yml
````

验证任务是否完成(Completed) </br>
kubectl get pod -n 命名空间 | grep -E "organizationusercompanyinit|installeruploader"
````
kubectl get pod -n ecnoo-pvt4 | grep -E "changecompanyproperties"
输出
changecompanyproperties-w7vvf       0/1     Completed   0          3d17h
````

如需重新执行修改租户属性任务， 则需先删除之前的任务
````
# 删除修改租户属性任务
kubectl delete -f  k8s_pvt/yml/base/changecompanyproperties.yml
````

###### 访问测试

部署完成，可以通过 kubectl get ingress -n 命名空间 查看部署的ingress， 确保域名正确并获取到正确的IP地址。
例如：
````
kubectl get ingress -n encoo-pvt4
NAME                           CLASS    HOSTS               ADDRESS     PORTS   AGE
console-web-v4-ingress         <none>  console.pvttest.com   IP地址       80    5d18h
apps-web-ingress               <none>  apps.pvttest.com      IP地址       80    5d18h
identity-ingress               <none>  auth.pvttest.com      IP地址       80    5d18h
apigateway-ingress             <none>  gateway.pvttest.com   IP地址       80    5d18h
apigateway-websocket-ingress   <none>  gateway.pvttest.com   IP地址       80    5d18h
````

所有域名添加记录解析， 客户端浏览器访问控制台前端站点URL:
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console41.png)
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console42.png)

部署完成后可备份部署相关文件并保存至本地
````
tar czf  k8s-consolev4pvt-4.1.136251.tar.gz hosts k8s_pvt playbooks roles
````

###### 其它操作
**清理**
当可通过kubectl操作需要部署的k8s集群时，可执行playbooks文件夹中的99.clean.yml文件一键清理部署的服务，任务以及配置文件。
````
ansible-playbook playbooks/99.clean.yml
````

执行完成后查看k8s命名空间下pod、service、configmaps、secret、ingress、job是否被清除。
````
kubectl get -n encoo-pvt4 pod,service,configmaps,secret,ingress,job
````



###### 相关问题

1. 上传流程包出错

上传流程包出错，通过F12调试控制台显示跨域错误</br>
Access to XMLHttpRequest at '对象存储的url地址' from origin 'xxx' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource 
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console43.png)

**解决方法:**</br>
对象存储配置跨域规则(一般联系客户配置)，例如
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console44.png)



2. 新建连接管理显示异常</br>
数据中心->连接管理->新建 显示异常</br>
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console45.png)
或者 文件服务->新建文件夹->绑定连接器-新建文件类连接 显示异常</br>
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console46.png)

**解决方法:**</br>
删除dataentity服务pod后让其重新生成pod</br>
````
kubectl get pod -n 命名空间 | grep dataentity
kubectl delete pod  -n 命名空间  pod名称kubectl delete pod  -n 命名空间  pod名称
````
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console47.png)

验证：</br>
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console48.png)
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console49.png)


##### 升级
1. 在部署机上清理之前的相关部署文件和目录，保留/etc/ansible/k8s_pvt/ssl目录 在部署机上清理之前的相关部署文件和目录，保留/etc/ansible/k8s_pvt/ssl目录
````
# 创建备份目录
mkdir /tmp/pvtbackup$(date +%F)
# 移动之前的相关部署文件和目录到备份目录(备份目录名称以实际为准)
cd  /etc/ansible
mv playbooks roles hosts /tmp/pvtbackupxxxx-xx-xx
mv k8s_pvt/yml /tmp/pvtbackupxxxx-xx-xx
````

> **说明：**
> 升级需保留/etc/ansible/k8s_pvt/ssl目录升级需保留/etc/ansible/k8s_pvt/ssl目录
/etc/ansible/目录下如果存在k8spvtpvtv4目录，请重命名为k8s_pvt目录v4目录，请重命名为k8s_pvt目录
> mv /etc/ansible/k8smv /etc/ansible/k8spvtpvtv4  /etc/ansible/k8s_pvtv4  /etc/ansible/k8s_pvt

2. 执行准备工作 执行准备工作
hosts文件中相关内容如无更改，需沿用之前部署时填写的内容。hosts文件中相关内容如无更改，需沿用之前部署时填写的内容。

3. 依次执行部署步骤2.1-2.4，注意数据库迁移必须在部署service服务之前完成 依次执行部署步骤2.1-2.4，注意数据库迁移必须在部署service服务之前完成。
> **说明：**
> 执行2.1的时候k8s_pvt/yml目录下不会生成idsrv4-cer.yml文件，所以也无需部署identityServer秘钥secret文件， 只需部署docker镜像服务器secret文件执行2.1的时候k8s_pvt/yml目录下不会生成idsrv4-cer.yml文件，所以也无需部署identityServer秘钥secret文件， 只需部署docker镜像服务器secret文件

4. 跳过2.5中的初始化公司及其管理员账户任务，执行上传安装包任务 跳过2.5中的初始化公司及其管理员账户任务，执行上传安装包任务

5. 访问测试 访问测试

##### kubectl常用命令
````
# 查看各类资源
kubectl get -n <namespace> pod|deployments|statefulset|configmaps|secrets|ingress 

# 查看具体某个资源的yaml文件，以pod为例
kubectl get -n <namespace> pod  <podname> -oyaml

# 部署yaml文件
kubectl apply -f <filename>|<dirname>
kubectl replace -f <filename>|<dirname>

# 获取pod详细信息
kubectl -n <namespace> describe pod <podname>

# 获取pod日志
kubectl -n <namespace> logs [-f] [-p] [-c containername] <podname> 

#进入容器
kubectl -n <namespace> exec -it <podname> [-c containername] bash

# 复制容器内/tmp/foo文件到本地
kubectl cp -c <containername> <some-namespace>/<some-pod>:/tmp/foo /tmp/bar

# 打印客户端和服务版本信息
kubectl version

````




### 备份
1. 单机版本控制台自带Mysql和Minio，用户可按需自行备份控制台部署路径下的Data文件夹，此文件夹中包含了单机版控制台所有所有的数据
2. swarm和k8s部署方案中，控制台服务依赖客户提供的数据库和对象存储集群。

### 如何做数据迁移
对于控制台版本升级造成的数据迁移需求，私有化安装包内自带了相关的数据迁移工具。单机版为自动执行，swarm和k8s部署方案文档内均有相关操步骤。

### 跨数据中心部署架构
多数据中心部署架构示意如下， 主要模式为主从备份和主主多活。

![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console50.png)

**如需详细讲解请联系我们：400-639-2198**


## 企业私有市场
1. 什么是私有市场
控制台（私有化部署和SAAS）的每一个租户默认自带有一个私有市场，无需客户自己安装。它和云扩公有市场类似，提供相同的服务，但其中的内容和工件属于客户私有。
2. 价值
减少用户使用私有市场路径，无需自己再配置

3. 私有市场包含：组件、流程和元素市场，没有代码市场

### 如何使用
在编辑器登录控制台账号后就可使用，可以发布和新建/打开私有市场中的组件、流程和元素项目。

- 发布
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console51.png)
- 新建/打开
![info](https://docimages.blob.core.chinacloudapi.cn/images/RunManger/0614-console52.png)
- 权限如何设置
目前所有人都可使用私有市场，暂无权限设置。

