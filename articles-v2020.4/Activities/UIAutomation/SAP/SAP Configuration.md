# SAP 自动化配置步骤

本功能仅在云扩企业版编辑器中支持。

> **说明：**
>
>- 录制/回放时，需保证产品与 SAP 客户端以同样的权限执行。
>- 在 RDP、Cirtrix 环境下操作 SAP 时，需以管理员权限启动 SAP（因为支持远程所启动的服务是以管理员权限执行的）。

## 启用 SAP WinGUI 脚本

`启用SAP WinGUI脚本并没有任何安全问题`
### 执行事务，修改参数

1. 打开 SAP 并登录连接
2. 执行事务代码 **RZ11**
3. 输入参数名 **sapgui/user_scripting**，按下回车键
4. **维护参数文件参数** 窗口中，参数名称输入 **sapgui/user_scripting**，点击 **显示**
5. 点击 **更改值**，**新值** 设置为 **TRUE**，**保存更改**
6. 重复第四步，分别将下述参数的值改为 **FALSE**
    - sapgui/user\_scripting\_disable\_recording
    - sapgui/user\_scripting\_force\_notification
    - sapgui/user\_scripting\_per\_user
    - sapgui/user\_scripting\_set\_readonly

    > **说明：**
    >
    > 事务 RZ11 中对参数的所有更改均立即生效，并且在系统重新启动时丢失。要使更改永久生效，请联系您的 SAP 系统管理员。

7. 注销后重新登录。

### 勾选启用脚本

1. 点击打开 **选项** 菜单

   ![选项菜单](https://docimages.blob.core.chinacloudapi.cn/images/Activities/itemmenu20210609.png)

2. 转到 **辅助功能与脚本** 后单击 **脚本**
3. 勾选 **启用脚本**

    ![启用脚本](https://docimages.blob.core.chinacloudapi.cn/images/Activities/script20210609.png)

4. 不勾选下述选项：
    - 在脚本附加到 SAP GUI 时发出通知
    - 在脚本打开连接时发出通知

    > **说明：**
    >
    > 当勾选启用脚本的操作步骤未执行时，会在运行流程时出现下图提示，请按照上述勾选启用脚本的步骤进行设置。

    ![注意](https://docimages.blob.core.chinacloudapi.cn/images/Amanda/SAPWarning.png)
