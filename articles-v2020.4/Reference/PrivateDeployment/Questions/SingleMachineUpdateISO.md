## 云扩私有化控制台(单机版)-更新服务镜像


### 背景

控制台相关服务均为容器化部署，使用docker镜像进行分发。对于已经部署在客户私有环境的控制台，可能存在由于问题修复和功能更新，需要替换部分服务镜像和修改配置的需求。



### 业务服务镜像

服务按业务可分为两大类，控制台相关服务和低代码相关服务。以下为各自对应的业务服务镜像。

- 控制台
  - 控制台前端镜像
    - encoo/console-web-v4-pvt
  - 基础服务镜像
    - encoo/digi4th-foundation-service
  - RPA服务镜像
    - encoo/rpa-service
    - encoo/rpa-rdp-service
    - encoo/rpa-rdp-web-service

- 低代码 （ViCode）
  - 低代码前端镜像
    - encoo/vicode-apps-web
  - 低代码服务镜像
    - encoo/vicode-service
    - encoo/vicode-collectionexecutor



> 控制台相关服务配置和定义文件位于控制台部署路径的根目录下，低代码服务的相关文件位于部署路径下的vicode文件夹中。由于文件组织的位置不同，故在更新镜像时需要修改的文件也略有差别。



### 更新步骤

以下以更新控制台前端站点镜像encoo/console-web-v4-pvt为例，控制台部署路径此处为/console/consolev4pvt-4.1.150431，具体操作时以实际为准

1.  准备镜像

      a.   上传到控制台服务器某个目录，此处为/console/consolev4pvt-4.1.150431/image目录下（镜		  像文件上传目录没有特定要求）

      b.   加载镜像

   ```
   1 #切换至镜像文件目录
   2 cd /console/consolev4pvt-4.1.150431/image
   3 #解压镜像文件（此处镜像文件扩展名为.tar.gz，需先解压，若镜像文件为.tar则忽略该步骤）
   4 tar -zxvf console-web-v4-pvt-4.1.76383.tar.gz
   5 # 加载镜像
   6 docker load -i ./console-web-v4-pvt-4.1.76383.tar
   ```

   ![加载镜像](https://docimages.blob.core.chinacloudapi.cn/images/8db01643-b388-44f2-9f7a-c563b68d75d9.png)

2. 修改系统配置文件.systemconfig中，对应镜像版本号（**<font color="red">若更新的为低代码相关镜像，则需修改vicode文件夹下的.systemconfig文件</font>**）

   ![修改系统配置文件](https://docimages.blob.core.chinacloudapi.cn/images/2dadc55b-6328-46a8-a0be-448321728d4c.png)

   > 请务必更新.systemconfig中的镜像版本号，否则有可能导致后续重启控制台后，镜像更新失效

3. 修改compose yml文件 (**<font color="red">由于开发迭代，老版本中可能不存在docker-compose.service.yml等yml文件，此时请按照下面的老版本文件修改方式操作</font>**)

   a. 新版本

   ​		  i. 修改docker-compose.service.yml文件中，对应服务image字段为需要更新的镜像版本名称。（**<font color="red">一般此处需要跟相关开发确认替换哪几个服务的镜像。当然也可将文件中相同的镜像名全部更新为新的tag</font>**）。例如，此处需要更新控制台前端服务，其镜像名为encoo/console-web-v4-pvt，则修改文件中的同名镜像的tag为上一步load命令显示的tag。

   ![新版本](https://docimages.blob.core.chinacloudapi.cn/images/c5a8519d-2e98-4a0c-9481-a900a521dc1e.png)

   > 若更新低代码服务镜像，则需要修改vicode文件夹下的docker-compose.yml文件

   b. 老版本

   ​		  i. 修改docker-compose.yml文件中，对应服务image字段为需要更新的镜像版本名称。

   ![老版本](https://docimages.blob.core.chinacloudapi.cn/images/21ad7a41-3579-48fc-a25f-e70f3f03d857.png)

4. 应用修改之后的yml

   ```
   1 # 切换到控制台部署目录下
   2 cd /console/consolev4pvt-4.1.150431/
   3 
   4 # 重新启动控制台(此命令会移除所有容器后，重新根据yml创建)
   5 ./deploy.sh restart
   ```

5. 执行docker ps -a，查看IMAGE列，服务是否已更新为新镜像![查看IMAGE列](https://docimages.blob.core.chinacloudapi.cn/images/cb90e061-f97e-42d7-8ccd-5778487b7c39.png)

