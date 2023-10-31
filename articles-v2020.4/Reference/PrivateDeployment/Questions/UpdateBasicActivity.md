## 云扩私有化控制台(单机版)-升级基础组件


### 背景

私有化控制台单机部署版本使用了一些开源基础组件，如mysql，redis，minio等。

出于稳定性因素考虑，一般不会频繁升级基础组件。但具体客户场景可能由于安全性的要求，需要升级基础组件到最新的版本，以应用一些安全性漏洞的修复。



> 升级基础组件有可能产生预料之外的兼容性问题，请谨慎升级或者备份相关文件，避免升级后无法降级。(例如，Mysql升级之后无法降级为低版本)



### 默认版本 && 镜像地址

- Mysql
  - 8.0.20-1debian10
  - <https://hub.docker.com/_/mysql>

- Redis
  - 6.0.5
  - <https://hub.docker.com/_/redis>
- Minio
  - RELEASE.2020-06-22T03-12-50Z
  - <https://min.io/download>
  - <https://github.com/minio/minio/releases>
- Nginx
  - 1.21.1+
  - <https://hub.docker.com/_/nginx>



>单机版控制台使用nginx作为前端站点服务器，前端镜像使用镜像构建时最新的nginx版本作为base镜像。若需要升级前端站点容器的nginx镜像，则须重新构建前端镜像而不能像其他组件一样单独升级



### 更新步骤



以下以更新Mysql镜像版本为例，控制台部署路径此处为/console/consolev4pvt-4.1.136251，具体操作时以实际为准

> 环境可访问外网，则忽略准备镜像的步骤，直接进行第二步。

1. 准备镜像                                                                                                                                                     a.   使用能访问外网机器，下载对应的镜像包

```
1 # 拉取指定版本镜像，此处拉取dockerhub上的mysql 8.0.28 
2 docker pull mysql:8.0.28
3 #docker pull redis:XXXXXXX
4 #docker pull nginx:XXXXXXX
5 #docker pull minio/minio:XXXXXXX
6
7
8 # 将镜像保存为tar包
9 docker save -o mysql-8.0.28.tar mysql:8.0.28
```

​	b.   上传到控制台服务器某个目录，此处为/console目录下                                                                     	c.	加载镜像

```
1 # 加载上一步上传到服务器上的镜像包
2 docker load -i /console/mysql-8.0.28.tar
```

2. 修改compose yml文件                                                                                                                             	a. 修改docker-compose.base.yml文件中，mysql服务image字段为需要更新的镜像版本名称，		例如升级Mysql镜像为8.0.28，其他组件同理

![figure 1](https://docimages.blob.core.chinacloudapi.cn/images/905b0cb0-828c-4e85-abf8-30d3f49f5385.png)

3. 更新基础组件

```
1 # 切换到控制台部署目录下
2 cd /console/consolev4pvt-4.1.136251
3 
4 # 重新deploy基础组件
5 ./deploy.sh deploybasic
6 
7 #对于老版本控制台，其部署脚本可能没有deploybasic选项，则可执行下面的命令来重新deploy基础组件
8 ./docker-compose --compatibility -p base -f docker-compose.base.yml -f docker-compose.baseoverride.yml up -d
```

