# 管理文件服务

## 文件夹管理

文件夹管理主要用于对各文件夹、子文件夹进行新建及删除等操作。文件服务中的文件必须存储于某一文件夹/子文件夹之内。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileervice1.png)

### 新建文件夹

点击左侧列表的“新建”按钮即可新建文件夹，新建出文件夹"命名框“自动处于可编辑状态，输入名称回车保存即可。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileservice2.png)

### 新建子文件夹

选择某一个文件夹，点击对应的”新建子文件夹“按钮即可再其结构下新增”子文件夹“。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileservice3.png)

### 删除文件夹&子文件夹

选择某一文件夹点击对应的”删除“按钮即可对该文件夹进行删除操作。

## 文件管理

### 上传文件

选择某一文件夹后点击对应的"上传"按钮后弹窗选择需要进行上传的文件即可在文件夹中上传文件。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/uploadfile.png)

### 文件上传过程管理

展示所有文件的上传过程，主要包括全部上传成功、部分上传成功、全部上传失败三种状态。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/uploadstatus.png)

### 下载文件

选择某一文件点击对应的”删除“按钮即经弹窗二次确认后可对该文件夹进行删除操作。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/downloadfile.png)

### 删除文件

选择某一文件点击对应的”删除“按钮即经弹窗二次确认后可对该文件夹进行删除操作。
![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/deletefile.png)

## 文件服务权限管理

文件服务权限按照一级文件夹进行配置，若用户对某一级文件夹具备某类权限，则对该一级文件夹下的所有文件夹或文件均具有相同权限。

### 打开权限编辑页面

点击一级文件夹操作选项中的“管理权限”按钮即可进入权限编辑页面， 编辑完成之后点击“保存”按钮即可。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileauthority1.png)

### 创建者权限

创建者即该文件夹的创建者，默认分配给其管理权限。

### 指定用户权限

指定用户权限可给不同用户赋予不同用户权限

1. 点击“添加”按钮可弹窗展现当前租户下所有可添加的用户列表。

2. 通过勾选方式选定需要添加的用户，点击“确定’按钮即可。

    ![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileauthority2.png)

3. 添加进之后默认给可读权限，通过下拉选择方式可对具体用户的权限进行修改。

    ![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileauthority3.png)

4. 点击用户名称前的“移除”按钮即可将对应的用户从指定用户列表中移除。

### 其他用户权限

其他用户指当前租户下除了创建者、指定用户列表之外的所有其他所有用户。默认给无权限，通过下拉选择方式可对权限进行修改。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileauthority5.png)
