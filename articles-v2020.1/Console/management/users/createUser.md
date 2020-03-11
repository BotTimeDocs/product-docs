# 新增用户
## 添加用户
进入全局设置-用户信息，点击新增按钮打开邀请用户弹窗。
![createuser](https://docimages.blob.core.chinacloudapi.cn/images/Console/users/createuser1.png)
请填写正确的用户姓名和邮箱，点击发送，系统将会向填写的邮箱发送一封邀请邮件。
![createuser](https://docimages.blob.core.chinacloudapi.cn/images/Console/users/createuser2.png)
发送成功后，系统会为你邀请的用户创建一个未激活账户，你可以在列表查看该用户。
![createuser](https://docimages.blob.core.chinacloudapi.cn/images/Console/users/createuser3.png)
未激活状态的用户无法登录控制台，用户需要通过邀请邮件激活他的账户（详见：[激活账户](/articles-v2020.1\Console\activeAccount.md)）
*邀请用户需要在72小时内激活账号，激活链接将在72小时后失效。若链接失效，你需要删除该未激活状态账号重新添加用户。

## 设置用户权限
添加用户后，需要赋予用户控制台的使用权限。否则用户将无法使用控制台的任何功能。使用权限分为两个级别:
- 资源组级别权限：详见给关于资源组
- 系统级别权限：
   - 配置：当前我们未开放系统级别权限的配置。这也就意味着，当前只有“系统管理员”可以使用系统级别权限。
   - 范围：一级菜单“全局管理”下的所有子菜单均为系统级别模块，当前仅“系统管理员”可见。
   - 系统管理员拥有本系统所有权限。

## 设置系统管理员
进入全局设置-用户信息，找到你希望设为系统管理员的用户。

选择列表操作：其他 - 设为系统管理员, 点击确认即可将用户设为系统管理员。设为系统管理员后，该用户即可享用本系统所有权限。
![setadmin](https://docimages.blob.core.chinacloudapi.cn/images/Console/users/setadmin.png)
你也可以在同样的位置取消用户的系统管理员权限。


<!-- 绑定角色（角色创建详见：[创建角色](../roles/createRoles)），以确保用户在激活后可以正常使用控制台。
点击编辑角色按钮，打开编辑角色弹窗。
 ![createuser](https://docimages.blob.core.chinacloudapi.cn/images/Console/users/createuser4.png)
点击角色选择框，你可以在下拉选项中看到角色管理的全部角色。
![createuser](https://docimages.blob.core.chinacloudapi.cn/images/Console/users/createuser4.png)
你可以通过点击选项，选中下拉列表中的角色
 ![createuser](https://docimages.blob.core.chinacloudapi.cn/images/Console/users/createuser6.png)
若角色过多，你可以通过角色选择框，输入角色名称，敲击回车进行模糊查询。
![createuser](https://docimages.blob.core.chinacloudapi.cn/images/Console/users/createuser7.png)
选择完角色后，点击保存，完成用户与角色的绑定。 -->
