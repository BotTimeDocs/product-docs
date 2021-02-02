# Windows屏幕解锁服务

## 案例介绍

有些 RPA 机器人流程自动化的触发，需要设置定时任务，在每天相同的时间里以不同的频次执行业务流程操作。如果机器人在启动的时候，电脑是锁屏状态，那么就会造成流程执行报错。

所以针对这种情况，现提供可使 RPA 机器人进行防锁屏运行的功能。

## 案例实现

编辑器或机器人在运行[锁屏](../../Activities/System/Screen/WindowsLockActivity.md)或[解锁](../../Activities/System/Screen/WindowsUnlockActivity.md)组件之前，需以**管理员身份**安装 **Windows 屏幕解锁服务**，以实现在 Windows 中自动化软件界面的操作。

1. **安装 Windows 屏幕解锁服务** </br>
  
   a. 以管理员身份运行**编辑器**或**机器人**应用。</br>
   b. 单击 Windows 屏幕解锁服务，进行安装。</br>

   >**说明：**
   >
   >- 编辑器中 Windows 屏幕解锁服务的入口：开始主页 > 工具。
   >- 机器人中 Windows 屏幕解锁服务的入口：设置 > 扩展。

2. **锁屏**</br>

    在流程中，需要执行锁屏的地方，拖入锁屏组件并设置其属性，以实现代替人工手动按下“Win+L”键后，但流程仍然在锁屏状态下运行。

3. **解锁**</br>

在流程中，需要执行解锁的地方，拖入解锁组件并设置其属性，以实现代替人工手动输入用户名和密码自动解锁电脑屏幕。

## 常见问题

1. **Windows 屏幕解锁服务支持安装在哪些操作系统中？**</br>
   目前支持的操作系统有 Windows 7、Windows 10、Windows Server 2008、Windows Server 2016、Windows Server 2019。

2. **如何卸载 Windows 屏幕解锁服务？** </br>
   步骤1：卸载程序入口：[卸载程序](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/EncooCredentialProviderUnInstall.bat)</br>
   步骤2：右击以管理员身份运行，卸载成功如下图所示。</br>
   ![Windows 屏幕解锁服务卸载完成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/uninstall20201202.png)</br>

3. **在 Windows 10系统中通过电子邮件在线帐号登录时，解锁组件中填写的用户名属性无效** </br>
   在解锁组件的“用户名”属性中填写在"C:\Users"目录下生成的以电子邮件在线帐号为名的文件夹名称。

4. **域用户登录时，在解锁组件中填写的用户名属性无效**</br>
   如果是域用户登录时，需要在解锁组件的用户名属性中填写{域名称\用户名称}，如：EncooFrank\Administrator

5. **企业版或 Server 版的操作系统锁屏后，在屏幕上出现了“按 Ctrl+Alt+Delete 解锁。”字样，是不支持自动解锁屏幕么？**</br>
    支持自动解锁屏幕，前提是需要在“控制面板 > 系统与安全 > 管理工具 > 本地策略”下找到“交互式登录：无需按Ctrl+Alt+Del”这一项，勾选“已启用”项。
