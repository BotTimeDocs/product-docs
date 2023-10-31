# 私有化控制台Swarm高可用版部署2.0
# 一. Swarm高可用部署文档

## 1.1 概况

##### 机器：10.10.10.1, 10.10.10.2, 10.10.10.3 三台服务器

##### 外部负载均衡器（F5或其他IP负载均衡）

##### 控制台私有化安装包

##### Redis4.x及以上版本

##### Mysql5.7及以上版本

##### S3接口对象存储

### 1.1.1 安装

#####  以下为模拟流程提供如下三台服务器

##### CentosA: 10.10.10.1

##### CentosB: 10.10.10.2

##### CentosC: 10.10.10.3

##### 云扩控制台安装包：consolev4pvt-4.1.141211

### 1.1.2 Docker离线安装

#### 安装方式：二进制安装

#### 版本：19.03.13

#### 安装文件：docker-19.03.13.tgz   docker.service   docker.socket

#### 下载docker安装文件：链接：[https://pan.baidu.com/s/106Rw-ZWSMTrEWGtTS-ymAQ](https://pan.baidu.com/s/106Rw-ZWSMTrEWGtTS-ymAQ) 

提取码：5ct3

#### 操作用户：root 

####   在CentosA,CentosB,CentosC 三台服务器上进行相同的操作，上传私有化控制台安装包，docker安装文件到服务器指定目录 /app 目录（也可自定义目录）；执行安装docker服务的命令

# 创建一个统一存放安装控制台的目录

cd  /

make  -p  app

#进入到该目录，把docker安装文件，控制台安装包通过sftp上传到该目录下面

#查看服务器防火墙状态，

systemctl status firewalld

#如果防火墙状态是running,开启的状态，执行命令，关闭防火墙

systemctl stop firewalld

#进入到app目录，安装docker服务

cd  /app

tar xf docker-19.03.13.tgz

cp docker/*  /usr/bin/

cp docker.socket  /etc/systemd/system/

cp docker.service  /etc/systemd/system/

systemctl daemon-reload

systemctl start docker.service

systemctl enable docker.service

systemctl status docker.service

#退出该状态

Ctrl+c

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-1.jpg)

## 1.2 Swarm 集群的搭建

#### 操作用户：root

### 1.2.1 CentosA服务器中进行以下操作，执行Swarm集群初始化的命令

#进入到app目录下面

cd  /app

# swarm集群初始化，创建Swarm集群

docker swarm init

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-2.jpg)

### 1.2.2 CentosB,CentosC 服务器中执行以下相同操作，执行节点加入Swarm集群的命令

#进入到app目录

cd  /app

#执行如下命令，加入到Swarm集群中，以下命令取自上一步执行结果的内容

docker swarm join --token SWMTKN-1-3qe4y4fz7wyhk6rzkbn3sdsx297ck7lrg0lxt3iqsdoh5y4zz1-0bgesujg10h2tpfzn5kxf69yp 172.18.0.16:2377

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-3.jpg)

### 1.2.3 CentosA 服务器上进入以下操作，查看Swarm 集群状态，执行集群节点加入管理集群节点的命令

#进入到app目录下面

cd  /app

#查看Swarm集群状态

docker  node  ls

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-4.jpg)

#设置集群管理节点，节点id取自上一步操作执行结果的id

  docker  node  promote  mdvemqwhj9sj04w0zmazans7i

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-5.jpg) 

 docker  node  promote  6uxufag8ihz9fx86bwl35zf6f

 ![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-6.jpg)

#设置完成后，类似于如下图  ![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-7.jpg)

## 1.3 控制台的部署

### 1.3.1 CentosA,CentosB,CentosC,三台服务器上进行以下相同的操作，执行加载镜像文件的命令

#进入到app目录

cd  /app 

#解压控制台压缩包consolev4pvt-4.1.141211

 tar  -zxvf  consolev4pvt-4.1.141211.tar.gz

#进入到控制台执行目录

 cd consolev4pvt-4.1.141211/swarm

#加载镜像

  sh  ha-deploy.sh  update

### 1.3.2 CentosA 服务器上进行以下操作，执行控制台初始化

根据Swarm高可用部署选择的访问负载均衡方式，初始化控制台访问域名部分的填写可以分为以下三种；

访问负载均衡方式的控制台目前有三种：1.多域名；2.域名+端口; 3.IP+端口 （以上三种访问方式，都需要在负载均衡中配置好转发策略）（第一种域名访问方式，需要申请五个域名，[控制台前端服务，授权认证服务，对象存储服务，API网关接入服务，小程序web前端服务]) (第二种域名+端口的访问 方式，至少需要申请一个域名）

实际域名和访问IP以客户提供为准，以下域名和IP都是举例

#### 控制台的初始化操作根据客户提供的资源，进行初始化操作

客户提供的资源：Mysql5.7及以上版本（必要）

                Redis4.x及以上版本（可选）

S3存储 （可选）(不能提供S3存储服务，需要提供NFS文件共享服务)

### 1.3.3访问方式为http的请求，执行控制台初始化操作

举例如下

第一种多域名访问

域名

www.consoleweb.com

www.appsweb.com

www.apigateway.com

www.sso.com

www.s3storage.com

服务访问地址

www.consoleweb.com(控制台前端服务域名);

www.appsweb.com(小程序web前端服务域名); 

www.apigateway.com(API网关接入服务域名); 

www.sso.com(授权认证服务域名);

www.s3storage.com(S3对象储存服务域名)

#控制台初始化， 

sh  ha-deploy.sh  init

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-8.png)

(注释:红框内容是根据客户提供的资源，选项存储对象和redis信息,此处是客户提供redis和存储服务; 是否填写外部对象存储和Redis，选择”Y”或者”N”以客户提供的资源为主)

第二种(域名+端口)访问

域名

www.rpadomain.com

默认端口 consolewebport>80  ssoport>81  appswebport>82  apigatewayport>8080  s3storageport>需要跟客户确认对方提供的存储服务端口$port，此处以9000端口举例）

服务访问地址

www.rpadomain.com(控制台前端服务域名); 

www.rpadomain.com:82(小程序web前端服务域名); 

www.rpadomain.com:8080(API网关接入服务域名);

www.rpadomain.com:81(授权认证服务域名);

www.rpadomain.com:$port(S3对象储存服务域名)

#控制台初始化

sh ha-deploy.sh init

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-9.jpg)

(注释:红框内容是根据客户提供的资源进行的选择，此处选择操作，客户提供了Redis，因为没有提供对象存储服务，使用的是安装包自带的Minio存储服务，所以客户要提供NFS文件共享服务；是否填写外部对象存储和Redis，选择”Y”或者”N”以客户提供的资源为主)

第三种(IP+端口)访问

负载均衡IP地址

52.131.87.118

默认端口 consolewebport>80  ssoport>81  appswebport>82  apigatewayport>8080  s3storageport>需要跟客户确认提供的存储服务的端口$port

服务访问地址

52.131.87.118(控制台前端服务访问地址); 

52.131.87.118:82(小程序web前端服务访问地址); 

52.131.87.118.82:8080(API网关接入服务地址);

52.131.87.118:81(授权认证服务访问地址);

52.131.87.118:$prot(S3对象存储服务访问地址。此次以9000端口举例)

#初始化控制台

sh ha-deploy.sh init

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-10.jpg)

(注释:红框内容是根据客户提供的资源进行的选择，此处选择操作，客户没有提供Redis和对象存储，Redis和对象存储使用的私有化安装包自带的。因为没有提供对象存储服务，使用的是安装包自带的Minio存储服务，所以客户要提供NFS文件共享服务；是否填写外部对象存储和Redis，选择”Y”或者”N”以客户提供的资源为主)

#### 查看初始化完成后的信息

#在执行初始化当前的目录，查看初始化完成后生成的信息（看下面红框的内容）

cat .userconfig

IP+端口访问方式：

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-11.jpg)

多域名访问方式：

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-12.jpg)

单域名访问方式：

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-13.jpg)

红框内容就是生成的访问各种服务的URL地址，实际地址以客户提供为准

#### 3.1.3 CentosA 服务器上进行以下操作，执行控制台的部署命令

#执行部署服务操作

sh ha-deploy.sh start

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-14.jpg)

### 1.3.4公司初始化，上传安装包命令操作

#查看服务是否全部启动，

docker service ls

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-15.jpg)  (注释：上图中 REPLICAS 列对应的副本数，斜杠左右两边数字一致，表明服务已全部启动)

#等服务全部启动成功之后，才能进行公司初始化操作命令

sh ha-deploy.sh organizationUserCompanyInit

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-16.jpg)

#执行上传安装包操作命令

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-17.jpg)

## 1.4 Swarm 高可用验证

### 1.4.1  CentosA 服务器上进行以下操作，执行查看服务状态的命令

#进入到app目录

cd  /app

# 查看Swarm服务状态

docker  service  ls

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-18.jpg)

REPLICAS 对应列，左右边的数值都保持相同了，说明服务已全部启动。

### 1.4.2 客户端浏览器访问控制台

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-19.jpg)

#在浏览器中输入登录地址

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-20.png)

## 1.5 高可用控制台的升级

### 1.5.1 CentosA 服务器上进行以下操作，停止服务

#进入到app目录

cd  /app 

#进入到控制台的执行目录

cd consolev4pvt-4.0.113501/swarm

#停止服务操作

sh ha-deploy.sh stop

### 1.5.2 在CentosA,CentosB,CentosC 三台服务器上进行相同的操作，上传最新私有化控制台安装包到/app目录(也可自定义目录),解压

#进入到app目录

cd /app

#解压新上传的私有化控制台安装包

tar -zxvf consolev4pvt-4.1.118041.tar.gz

### 1.5.3 在CentosA,CentosB,CentosC 三台服务器上进行相同的操作,加载镜像

#进入到控制台目录

cd consolev4pvt-4.1.118041/swarm/

#进行加载镜像操作

sh ha-deploy.sh update

### 1.5.4 CentosA 服务器上进行控制台初始化操作

#进入到控制台目录

cd  /app/ consolev4pvt-4.1.118041/swarm

#原有控制台初始化操作，是按照init 参数，现在的控制台就按照以下操作命令进行

sh ha-deploy.sh init

#原有控制台初始化操作，是按照initmore参数，现在的控制台就按照以下操作命令进行

sh ha-deploy.sh initmore

### 1.5.5 CentosA 服务器上进行数据迁移操作

#进入到控制台目录

cd  /app/ consolev4pvt-4.1.118041/swarm

#执行数据迁移操作

sh ha-deploy.sh dataMigrationFoundation

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-21.png)

sh ha-deploy.sh dataMigrationVicode

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-22.png)

### 1.5.6 CentosA 服务器上进行启动控制台服务操作

#进入到控制台目录

cd  /app/ consolev4pvt-4.1.118041/swarm

#控制台开始部署,执行部署命令操作

sh ha-deploy.sh start

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-23.jpg)

### 1.5.7 公司初始化，上传安装包命令操作

#查看服务是否全部启动，

docker service ls

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-24.jpg)

(注释：上图中 REPLICAS 列对应的副本数，斜杠左右两边数字一致，表明服务已全部启动)

#等服务全部启动成功之后，才能进行公司初始化操作命令

sh ha-deploy.sh organizationUserCompanyInit

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-25.jpg)

#执行上传安装包操作命令

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-26.jpg)

### 1.5.8 客户端浏览器访问控制台

#打开浏览器输入登录地址

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-27.jpg)

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-28.png)

# 二. 常规需求

## 2.1 部署控制台非root 账号部署方案解决

### 创建的appuser普通用户加入docker组

#### 操作用户：root

#### 在CentosA,CentosB,CentosC 三台服务器上执行以下相同的操作，执行非root账户加入docker组的命令

groupadd  docker

gpasswd  -a  rpauser   docker

systemctl  restart docker

chmod  a+rw  /var/run/ docker.sock

#操作完成之后，就可以切换到普通用户进行控制台的部署

## 2.2 服务器文件根目录空间不够用

### docker根目录修改

#### 操作用户：root

#### 在CentosA,CentosaB,CentosC 三台服务器上进行以下相同的操作，执行转移docker根目录的命令

#进入到app目录下面，创建docker目录

make -p  Dockerdir

# 查询 docker服务所在位置

docker info |grep “Dodcker Root Dir”

例如docker所在目录 

 /var/lib/docker

#停止docker 服务

systemctl stop docker.service

#移动到指定目录文件中   /app/Dockerdir

mv  /var/lib/docker/   /app/Dockerdir/

#创建软连接

ln -s  /app/Dockerdir/docker/   /var/lib

#重新启动docker服务

systemctl  start  docker.service
# 三. 控制台Docker Swarm部署负载均衡转发说明
## 3.1 概述

RPA控制台Swarm高可用最少采用三节点部署，控制台将部分服务的容器端口映射到每台主机的对应端口。服务域名均解析到负载均衡IP，负载均衡需根据域名将请求转发到后端任意一台服务器的对应端口。

下面将以三节点Swarm部署方案说明具体转发策略

假设后端三台服务器分别为：10.24.72.130，10.24.72.131，10.24.72.132

相关服务的域名及对应端口如下：

1.  控制台前端站点
    
    -   域名：console.encoo.com
        
    -   服务器端口：80
        
2.  单点登录服务
    
    -   域名：auth.encoo.com
        
    -   服务器端口：81
        
3.  低代前端站点
    
    -   域名：apps.encoo.com
        
    -   服务器端口：82
        
4.  接口网关服务
    
    -   域名：api.encoo.com
        
    -   服务器端口：8080
        

## 3.2 服务转发规则

![](https://docimages.blob.core.chinacloudapi.cn/images/Sself-29.png)

如上图所示，控制台所需四个域名均解析到负载均衡IP。

负载均衡需配置如下规则（以下配置均采用nginx举例，实际配置信息以所采用的具体LB为准）：

-   控制台前端站点
    
    -   域名为 console.encoo.com 的请求，转发至后端任意一台服务器的80端口。
        
    -   后端服务器及端口：10.24.72.130:80，10.24.72.131:80，10.24.72.132:80
        

```
# nginx 转发示例
upstream console-web{
    #ip_hash;
    server 10.24.72.130:80 max_fails=2 weight=1;
    server 10.24.72.131:80 max_fails=2 weight=1;
    server 10.24.72.132:80 max_fails=2 weight=1;
    check interval=5000 rise=1 fall=3 timeout=3000 default_down=false;
 }

server {
    listen       443 ssl;
    listen  [::]:443 ssl;
    server_name  console.encoo.com;

    ssl_certificate      consoleweb.crt;
    ssl_certificate_key  consoleweb.key;

    location / {
        proxy_set_header Host $http_host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_pass   http://console-web/;
    }
}
```

-   单点登录服务
    
    -   域名为 auth.encoo.com 的请求，转发至后端任意一台服务器的81端口。
        
    -   后端服务器及端口：10.24.72.130:81，10.24.72.131:81，10.24.72.132:81
        

```
# nginx 转发示例
upstream console-auth{
    #ip_hash;
    server 10.24.72.130:81 max_fails=2 weight=1;
    server 10.24.72.131:81 max_fails=2 weight=1;
    server 10.24.72.132:81 max_fails=2 weight=1;
    check interval=5000 rise=1 fall=3 timeout=3000 default_down=false;
 }


server {
    listen       443 ssl;
    listen  [::]:443 ssl;
    server_name  auth.encoo.com;

    ssl_certificate      consoleauth.crt;
    ssl_certificate_key  consoleauth.key;

    location / {
        proxy_set_header Host $http_host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_pass   http://console-auth/;
    }
}
```

单点登录服务转发规则需要带上X-Forwarded相关Header，服务依赖此Header获取当前请求真正的Proto，用于提供正确的oidc发现文档

-   接口网关服务
    
    -   域名为 api.encoo.com 的请求，转发至后端任意一台服务器的8080端口。
        
    -   后端服务器及端口：10.24.72.130:8080，10.24.72.131:8080，10.24.72.132:8080
        

```
# nginx 转发示例
upstream console-gateway{
    #ip_hash;
    server 10.24.72.130:8080 max_fails=2 weight=1;
    server 10.24.72.131:8080 max_fails=2 weight=1;
    server 10.24.72.132:8080 max_fails=2 weight=1;
    check interval=5000 rise=1 fall=3 timeout=3000 default_down=false;
 }


server {
    listen       443 ssl;
    listen  [::]:443 ssl;
    server_name   api.encoo.com;

    ssl_certificate      consolegateway.crt;
    ssl_certificate_key  consolegateway.key;

    location / {
        proxy_set_header Host $http_host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
				proxy_set_header Upgrade $http_upgrade; //机器人与控制台使用websocket通信，nginx需要配置支持websocket
        proxy_set_header Connection upgrade; //同上
        proxy_pass   http://console-gateway/;
    }
}
```

接口网关服务转发规则需要支持WebSocket长连接，机器人与控制台使用WebSocket通信

-   低代前端站点
    
    -   域名为 apps.encoo.com 的请求，转发至后端任意一台服务器的82端口。
        
    -   后端服务器及端口：10.24.72.130:82，10.24.72.131:82，10.24.72.132:82
        

```
# nginx 转发示例
upstream apps-web{
    #ip_hash;
    server 10.24.72.130:82 max_fails=2 weight=1;
    server 10.24.72.131:82 max_fails=2 weight=1;
    server 10.24.72.132:82 max_fails=2 weight=1;
    check interval=5000 rise=1 fall=3 timeout=3000 default_down=false;
 }


server {
    listen       443 ssl;
    listen  [::]:443 ssl;
    server_name   apps.encoo.com;
  
    ssl_certificate      appsweb.crt;
    ssl_certificate_key  appsweb.key;

    location / {
        proxy_set_header Host $http_host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_pass   http://apps-web/;
    }
}
```