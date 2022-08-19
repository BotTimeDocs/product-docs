# 私有化控制台V4部署手册

## 1.1Docker 环境准备(基于centos7)

#### 1.1.1.1 获取docker-ce yum源文件-repo

1. 登录到centos7服务器（root特权用户）;</br>
2. 命令行: cd /etc/yum.repos.d/   切换到repo文件保存的目录;</br>
3. 使用wget或者curl命令下载repo文件
   `wget https://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo`
或者
`curl -o docker-ce.repo  https://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo`  </br>
4. 执行yum makecache fast 生成缓存 并 执行yum repolist 查看docker源是否已经在其中</br>
![syh001](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0001.png)
</br>

#### 1.1.1.2安装docker-ce

命令行执行：`yum install docker-ce -y`，完成后执行`docker --version` 查看docker是否已经成功安装已经所安装的版本
</br>
![syh002](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0002.png)

#### 1.1.1.3启动docker并设置为开机自动启动

启动docker   `systemctl start docker`

开机自动启动 `systemctl enable docker`

重启docker   `systemctl restart docker`

#### 1.1.1.4验证安装

验证 Docker CE 安装是否正确，可以运行 hello-world 镜像:`docker run hello-world`，出现红框中的文字说明docker 的环境以及就绪:

![syh003](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0003.png)

#### 1.1.1.5安装docker-compose

下载docker-compose 可能执行文件
`curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
</br>
再为docker-compose添加可执行权限
`chmod +x /usr/local/bin/docker-compose`
</br>
最后为docker-compose做一个软链接
`ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose`

#### 1.1.1.6 验证docker-compose安装
命令行: 

`docker-compose  --version`

![syh004](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0004.png)

### 1.1.2 离线安装(断网环境)

#### 1.1.2.1 创建离线软件包存档目录

在服务器上创建目录dockerrpm以及dockercompose

`mkdir -p /docker/dockerrpm`

`mkdir -p /docker/dockercompose`

#### 1.1.2.2 将docker离线安装包及docker-compose软件包上传到指定目录

将docker安装包docker.ta.gz上传到/docker/dockerrpm/下，再将docker-compose上传到/docker/dockercompose/

#### 1.1.2.3 安装docker及docker-compose

`cd /docker/dockerrpm/`
`tar xf docker.tar.gz` #该步骤会解压出来大量rpm包
然后执行
`yum install -y *.rpm`

`cd /docker/dockercompose/`

`cp docker-compose /usr/bin/`

`chmod +x /usr/bin/docker-compose`

#### 1.1.2.4 启动docker进程并验证docker及docker-compose

启动docker

`systemctl start docker`

`systemctl enable docker`

`docker --version` #查看docker版本

`docker-compose --version` #查看docker-compose版本

## 1.2 Docker环境准备(ubuntu 18.04)

### 1.2.1 在线安装
如果使用的是root用户则不用加sudo
#### 1.2.1.1 更新apt包索引
`sudo apt-get update`
#### 1.2.1.2 安装软件包以允许apt通过HTTPS使用存储库
`sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
software-properties-common`

#### 1.2.1.3 添加Docker的官方GPG密钥
`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add –`

#### 1.2.1.4 设定docker稳定版存储仓库
`sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"`

#### 1.2.1.5 更新apt包索引

`sudo apt-get update`

#### 1.2.1.6 安装docker-ce

`sudo apt-get install docker-ce docker-ce-cli containerd.io`

### 1.2.2 离线安装

#### 1.2.2.1 确认客户的Ubuntu版本

查看Ubuntu系统版本命令

`cat /proc/version`

![syh005](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0005.png)

再下载对应版本的deb包https://download.docker.com/linux/ubuntu/dists/
以18.04为例https://download.docker.com/linux/ubuntu/dists/bionic/pool/stable/amd64/
#### 1.2.2.2 下载3个deb包并上传到Ubuntu服务器
`containerd.io_1.2.6-3_amd64.deb`

`docker-ce_19.03.5_3-0_ubuntu-bionic_amd64.deb`

`docker-ce-cli_19.03.5_3-0_ubuntu-bionic_amd64.deb`

#### 1.2.2.3 安装docker
`sudo dpkg -i *.deb`

## 2.1 部署控制台（基于Centos7）

### 2.1.1 上传私有化部署控制台需要的镜像文件到服务器

以consolev4pvt-4.0.87971.tar.gz私有化包为例
`mkdir -p /console`
上传consolev4pvt-4.0.87971.tar.gz到/console
解压consolev4pvt-4.0.87971.tar.gz

`tar -zxvf consolev4pvt-4.0.87971.tar.gz`

![syh006](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0006.png)

### 2.1.2 关闭防火墙和SELINUX，并重启docker服务
`systemctl stop firewalld`

`setenforce 0`

`service docker restart`

### 2.1.3 添加deploly.sh的执行权限
`cd consolev4pvt-4.0.87971/`

`chmod +x deploy.sh`

![syh007](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0007.png)

### 2.1.4初始化配置
`sh deploy.sh init`

![syh008](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0008.png)

### 2.1.5 加载镜像并启动（这一步可能会等待超过10分钟）
`sh deploy.sh start`

![syh009](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh0009.png)

### 2.1.6 使用默认管理员账号登录 
用户名:admin@encootech.com

密码:123456

租户名称:encoo

数据库用户:consoleuser,密码:Encoo123!@#

redis密码:Encoo123!@#

MINIOAccessKey:encoouser,MINIOSecretKey:Encoo123!@#

![syh0010](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00010.png)

## 3.1常用命令

### 3.1.1查看正在运行的docker容器

`docker ps`

![syh0011](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00011.png)

### 3.1.2结束正在运行的docker容器

`docker kill 8c814735ccc9`

![syh0012](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00012.png)

### 3.1.3 docker-compose启动/停止容器
`docker-compose start/stop`

### 3.1.4 修改日志配置
使用条件：项目start过至少1次之后
`./deplay.sh logConfig`

![syh0013](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00013.png)

修改之后使用命令重启服务：
`./deplay.sh restart`

## 4.1 升级控制台
控制台依赖Mysql和Minio来持久化业务相关数据。若想在控制台升级后保留原有数据，则需将原有控制台的mysql和minio持久化文件夹，拷贝到新版本控制台的对应路径下。

> 控制台私有化包自4.0.97891版本之后，变更了持久化数据的存储位置，将mysql，minio等放在了同一个data文件夹下，方便统一管理。故在copy老版本控制台业务数据至新版本目录下时，须根据实际目录情况将mysql/minio对应数据拷贝至指定目录。
即
`dbdata → data/mysql/dbdata`
`miniostorage → data/minio`
或`data → data`

新老版本持久化数据目录如下：

1. 老版本目录结构
   
   ![syh0014](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00014.png)
   
   ● dbdata：MySql持久化数据
   
   ● miniostoarge：Minio持久化数据
   
2. 新版结构目录
   
   ![syh0015](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00015.png)

   ● data/mysql/dbdata：MySql持久化数据
   
   ● data/minio：Minio持久化数据

### 4.1.1停止并移除旧控制台镜像
停止并删除所有容器

`docker rm -f $(docker ps -aq)`

### 4.1.2 将老版本控制台下mysql，minio等持久化数据拷贝到新版控制台目录下对应路径
cd到新版本控制台目录下，执行以下命令将mysql/minio数据拷贝到新版本控制台中。

1. 拷贝dbdata目录至data/mysql下
`cp -R Console-Old/dbdata/ ./data/mysql/`

2. 拷贝miniostoarge数据至data/minio下
`cp -R Console-Old/miniostorage/* ./data/minio/`

或

拷贝data目录至当前新版本控制台下
`cp -R Console-Old/data/ ./`



### 4.1.4给deploy.sh执行权限，执行初始化
`chmod +x deploy.sh`

`sh deploy.sh init`

![syh0016](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00016.png)

### 4.1.5启动服务
`sh deploy.sh start`

![syh0017](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00017.png)

### 4.1.6 清除localstorage
浏览器打开旧地址，使用F12开发者工具，找到旧登录地址的localstorage，右键清除localstorage（两个都要清）

![syh0018](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/syh00018.png)

### 4.1.7 重新登陆
重新刷新旧登录地址，用旧控制台账号登录（忽略部署完成后linux的提示，账号和流程都是和旧控制台一致）