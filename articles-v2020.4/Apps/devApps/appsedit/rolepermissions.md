# 角色权限

**角色权限**支持为不同用户设置不同角色。通过用户所属的角色权限，管控用户可以查看的页面以及可以操作数据的范围。例如，IT 管理员可以查看所有页面和数据，普通员工则只能查看自己的数据。HR 部门只有特定人员可以查看员工的工资字段，而其他人员只能查看员工的基本信息等等。

此外，还可以通过设置“匿名访问”，用户无需登录即可访问应用的页面和数据。

## 内置角色

角色权限里内置了“超级管理员”和“匿名角色”：
- **超级管理员**默认可以访问应用内的所有页面和数据源方法，如不满足可重新定义新的角色。
- **匿名角色**默认可以访问应用内的所有页面和数据源方法，支持调整权限配置。
  
>**说明：**
>
>匿名角色仅当开启”匿名访问“后才会显示，且仅支持一个匿名角色。

## 新建角色

在“角色权限”视图，单击“新建”，打开新建窗口
1. 设置角色基本信息后，单击“下一步”

    ![基本信息](https://docimages.blob.core.chinacloudapi.cn/images/Kris/newrole1.jpg)

2. 设置角色可访问的页面和数据源权限后，单击“下一步”

    ![权限配置](https://docimages.blob.core.chinacloudapi.cn/images/Kris/newdrole2.jpg)

3. 为该角色添加用户后，单击“确定”即可新建角色

    ![用户管理](https://docimages.blob.core.chinacloudapi.cn/images/Kris/newrole3.jpg)

## 编辑角色

在“角色权限”视图，选中任一角色，单击“编辑”进入角色详情页编辑角色。

![编辑角色](https://docimages.blob.core.chinacloudapi.cn/images/Kris/editrole.jpg)


## 删除角色 

若你想要删除角色：
1. 在“角色权限”视图，选中任一角色，单击“删除”
2. 在打开的二次确认弹窗内，单击“确定”，即可删除数据源

![删除角色](https://docimages.blob.core.chinacloudapi.cn/images/Kris/deleterole.jpg)

## 角色权限

### 页面访问权限
当相应角色配置了页面访问权限后，角色关联的用户即可以访问对应页面。

![页面访问权限](https://docimages.blob.core.chinacloudapi.cn/images/Kris/pagepermission.jpg)

>**说明：**
>
>页面访问权限配置仅当保存应用后生效
>
>用户关联的角色没有勾选可以访问的页面，预览或使用应用时访问未勾选的页面，则会展示空白页，并提示“当前页面没有访问权限”

### 数据源方法权限

当相应角色配置了数据源方法权限后，角色关联的用户才可以对数据源进行相应操作，比如数据的增删改查。

![数据源权限](https://docimages.blob.core.chinacloudapi.cn/images/Kris/pagepermission.jpg)

>**说明：**
>
>用户关联的角色没有勾选数据源方法权限，预览或使用应用时触发未勾选的数据源方法，则提示“当前无操作权限”


