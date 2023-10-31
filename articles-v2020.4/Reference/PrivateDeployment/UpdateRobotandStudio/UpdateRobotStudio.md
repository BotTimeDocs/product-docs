## 机器人和编辑器安装程序升级文档


### 1.下载安装程序

选择需要的版本号，分别下载需要升级的编辑器安装程序文件和机器人安装程序文件， 这里以1.1.2109.17为例，下载机器人安装程序文件和编辑器安装程序文件

- [最新版编辑器](https://encoorpabuild.blob.core.chinacloudapi.cn/bottimeinstallers/release-lts/lts/enterprise/1.1.2206.12/ide/Encoo.Studio.Setup.exe?sv=2018-03-28&sr=b&sig=Fh6rNhDJh0B3E8VcLSpGMO4ymkqCKk4QFdKBUjuX08c%3D&se=2022-08-24T04%3A59%3A55Z&sp=r)

- [最新版机器人](https://encoorpabuild.blob.core.chinacloudapi.cn/bottimeinstallers/release-lts/lts/enterprise/1.1.2206.12/robot/Encoo.Robot.Setup.exe?sv=2018-03-28&sr=b&sig=JHwLsUAV%2B%2FGDz888yHT2VHnPqhMEjcnu5bylVxi1%2BwM%3D&se=2022-08-24T04%3A59%3A57Z&sp=r)


### 2. 上传安装程序文件

进入私有化安装包中的安装程序上传目录，底下有robot和studio2个目录

```
1 cd consolev4pvt-4.0.103661/tools/InstallerUploadTool/Program/InstallerUploader/package
```

![安装程序上传目录](https://docimages.blob.core.chinacloudapi.cn/images/7173e159-ead9-4966-a508-9e63a9da977f.png)



进入robot目录，清空目录，上传之前下载的机器人安装程序文件到此目录

```
1 cd robot
2 rm * -rf
```

![robot目录](https://docimages.blob.core.chinacloudapi.cn/images/34248f63-0eca-4741-88d6-df62ca38d5a3.png)

进入studio目录，清空目录，上传之前下载的编辑器安装程序文件到此目录

```
1 cd studio
2 rm * -rf 
```

![studio目录](https://docimages.blob.core.chinacloudapi.cn/images/1ecca17d-d7a7-4fca-a4ef-98815036c75e.png)



### 3. 修改配置文件

返回私有化部署安装包目

![返回私有化部署安装包目](https://docimages.blob.core.chinacloudapi.cn/images/6c046025-74c6-4a48-aac2-18ba3bcec432.png)



修改配置文件

```
1 # 把配置文件中的1.1.2108.9修改成1.1.2109.17，共计有6个地方
2 vim tools/InstallerUploadTool/Program/InstallerUploader/config.json
3 
4 "PackageName": "云扩RPA编辑器(企业版)",
5 ...
6 "Version": "1.1.2108.9",
7 "FileName": "Encoo.Studio-1.1.2108.9-full.nupkg",
8 "FilePath": "package/studio/Encoo.Studio-1.1.2108.9-full.nupkg"
9 
10 "PackageName": "云扩RPA机器人(企业版)",
11 ...
12 "Version": "1.1.2108.9",
13 "FileName": "Encoo.Robot-1.1.2108.9-full.nupkg",
14 "FilePath": "package/robot/Encoo.Robot-1.1.2108.9-full.nupkg"
```

### 4. 单机版升级安装程序

返回私有化部署安装包目，执行升级命令

```
1 ./deploy.sh upload
```

当linux控制台输出 "上传安装包完成 " 则代表升级安装程序成功

![上传安装包完成](https://docimages.blob.core.chinacloudapi.cn/images/330f9267-b8b9-4aac-91e3-a38eaecc08ef.png)



登录控制台，下载升级后的编辑器和机器人安装程序

![安装包下载](https://docimages.blob.core.chinacloudapi.cn/images/28d45579-f178-4409-b37c-e5e51eca6b2e.png)



### 5. k8s升级安装程序

#### 构建上传安装包镜像

进入私有化部署安装包目下的k8s目录， 编辑hosts文件，确保镜像服务器地址信息已填写，构建镜像

```
1 vim hosts
2 # 配置镜像仓库的的secret
3 ...
4 DOCKER_SERVER="xxx.harbor.com/pvt"
5 
6 
7 # 构建镜像
8 sh init.sh build
```

镜像构建完成后可通过docker push 镜像名称:tag 命令上传到指定镜像仓库。

#### 重新上传安装程序

如需重新上传安装程序， 则需先删除之前的任务

```
1 kubectl delete -f k8s_pvt_v4/yml/base/organizationusercompanyinit.yml
2 或者
3 kubectl delete job organizationusercompanyinit 
```

执行上传安装程序任务

```
1 kubectl apply -f k8s_pvt_v4/yml/base/organizationusercompanyinit.yml
```

通过 kubectl logs installeruploader-xxxxx 查看上传安装程序执行结果， 如日志最后为completed则上传安装程序成功

登录控制台，下载升级后的编辑器和机器人安装程序

![安装包下载](https://docimages.blob.core.chinacloudapi.cn/images/bbae7bdc-0048-4f91-b261-41ddff6f260a.png)

