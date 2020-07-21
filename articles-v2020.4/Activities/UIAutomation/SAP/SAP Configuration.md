# SAP 自动化配置步骤

本功能仅在云扩企业版编辑器中支持。

## 启用SAP WinGUI脚本 
`启用SAP WinGUI脚本并没有任何安全问题`
### 执行事务，修改参数
1. 打开SAP并登录连接
2. 执行事务代码**RZ11**
3. 输入参数名 **sapgui/user_scripting**，按下回车键
4. **维护参数文件参数**窗口中，参数名称输入**sapgui/user_scripting**，点击**显示**
5. 点击**更改值**，**新值**设置为**TRUE**，**保存更改**
5. 重复第四步，分别将下述参数的值改为**FALSE**
    - sapgui/user\_scripting\_disable\_recording
    - sapgui/user\_scripting\_force\_notification
    - sapgui/user\_scripting\_per\_user
    - sapgui/user\_scripting\_set\_readonly

    注意：事务RZ11中对参数的所有更改均立即生效，并且在系统重新启动时丢失。要使更改永久生效，请联系您的SAP系统管理员。

6. 注销后重新登录 

### 勾选启用脚本 
1. 点击打开**选项**菜单
2. 转到**辅助功能与脚本**后单击**脚本**
3. 勾选**启用脚本**
4. 不勾选下述选项：
    - 在脚本附加到 SAP GUI 时发出通知
    - 在脚本打开连接时发出通知





