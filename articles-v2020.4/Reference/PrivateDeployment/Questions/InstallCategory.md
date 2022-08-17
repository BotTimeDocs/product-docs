## 控制台安装包目录结构说明



### 概述

云扩RPA控制台支持多种方式的私有化部署，这些方式的相关部署文件均包含在控制台安装包中。本文档主要对私有化安装包的目录结构做概括性的说明。



### 目录结构

```
1 .
2 ├── .common #单机部署通用文件
3 │   ├── config #单机版默认参数配置
4 │   ├── templates #单机版部署文件模板
5 │   └── tools #单机版帮助工具
6 ├── data #单机版控制台持久化文件目录
7 │   ├── id4_cert #单点登录token签名证书(部署过程中生成)
8 │   ├── minio #对象存储服务Minio持久化文件目录
9 │   ├── mysql #数据库Mysql持久化文件目录
10 │   └── ssl #https部署时，ssl证书目录
11 ├── deploy.sh #单机版部署脚本
12 ├── docker-compose #docker-compose二进制文件
13 ├── docker-compose.baseoverride.yml #单机版基础组件yml(用于重写动态的配置，例如端口，账号密码等)
14 ├── docker-compose.base.yml #单机版基础组件yml
15 ├── docker-compose.serviceoverride.yml #单机版控制台服务yml,(用于重写动态的配置，例如端口等)
16 ├── docker-compose.service.yml  #单机版控制台服务yml
17 ├── dockerinit.sh
18 ├── image #控制台镜像文件夹
19 │   └── console.tar #控制台镜像文件
20├── Info
21 │   └── README.txt #控制台镜像分支信息
22 ├── k8s # k8s部署文件夹
23 │   ├── hosts #k8s部署自定义参数文件
24 │   ├── init.sh #k8s部署帮助脚本
25 │   ├── playbooks #k8s部署ansible playbooks文件夹
26 │   ├── README.md #k8s部署REAMME文件
27 │   ├── roles #k8s部署ansible roles文件夹
28 │   └── tools #k8s部署相关工具
29 ├── logs #单机版控制台，控制台服务日志文件夹
30 ├── mysql-ha # mysql主从
31 │   └── mysql-ha.tar.gz
32 ├── pvtconfig #控制台服务配置文件夹(主要包含配置template，和根据.userconfig从配置模板生成的服务配置)
33 │   ├── appsettings_apigateway.json #例如，此为gateway服务配置文件
34 │   ├── appsettings_apigateway.template.json #例如，此为gateway服务配置文件模板
35 │   ├── ... #略
36 │   ├── ingress #需要部署反向代理时，nginx配置文件
37 │   ├── wait-for-it.sh #docker compose部署工具脚本
38 │   └── wait-for-it.template.sh #docker compose部署工具脚本模板
39 ├── swarm #docker swarm多节点部署文件夹
40 │   ├── Cert #单点登录token签名证书(部署过程中生成)
41 │   ├── ha-deploy.sh #docker-swarm部署脚本
42 │   ├── ha-docker-swarm.template.yml #docker swarm部署服务yml
43 │   ├── ha-minio.template.yml #对象存储服务minioyml模板，用于客户无法提供对象存储服务时，配合nfs搭建对象存储
44 │   ├── ha-nat.template.yml #rpa远程桌面服务yml模板
45 │   ├── ha-redis.template.yml #redis服务yml模板
46 │   ├── logs # docker swarm部署，服务日志文件夹
47 ├── tools #部署工具
48 │   ├── InstallerUploadTool #编辑器/机器人安装包上传工具
49 │   ├── LogFileConfig #业务服务日志文件配置工具
50 │   ├── Monit #单机版磁盘用量监控工具
51 │   ├── V2OrganizationUserCompanyInit #控制台账号及组织初始化工具
52 │   └── V4DataMigrationTools #控制台服务升级数据迁移工具
53 ├── v1deploy.sh #控制台服务部署脚本v1(弃用)
54 ├── v2deploy.sh #控制台服务部署脚本v2
55 ├── .userconfig #单机版部署参数用户配置文件
56 ├── .systemconfig #单机版系统变量为年间
57 ├── .env #docker compose环境变量文件
58 └── vicode #低代码(ViCode)服务部署文件夹
59     ├── config #低代码服务配置文件
60     ├── deploy.sh #低代码服务部署脚本
61     ├── docker-compose.override.none_ssl_template.yml #单机版低代码服务非https部 署yml模板
62     ├── docker-compose.override.yml #单机版低代码服务部署yml
63     ├── docker-compose.template.yml #单机版低代码服务部署yml模板
64     ├── docker-compose.yml #单机版低代码服务部署yml
65     ├── image #低代码服务镜像
66     ├── logs #单机版低代码服务日志文件夹
67     └── tools #低代码服务部署工具
68


```

> - 环境不同，控制台的部署参数不同，部署文件名称中含有【template】，一般为模板文件。部署时会结合用户配置，生成实际的部署文件
> - 服务定义yml，文件名中含有override的文件通常定义了一些可变的部分，例如接口等