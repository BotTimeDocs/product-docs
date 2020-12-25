# 解锁
解锁系统屏幕，进入系统桌面。
>**说明：**
>
>运行此组件前，需安装 [Windows 屏幕解锁服务](Studio/../../../../Studio/Extensions/WindowsUnlockService.md)扩展。

## 属性

### 基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件。
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件。


### 输入
- **用户名**：登录系统的用户名或微软帐户，可接变量。
- **密码**：登录系统的密码（微软帐户需要输入微软帐户的密码），可接变量。
  
## 操作示例
1. 拖入一个**解锁**组件至流程（已有**锁屏**组件的流程）中。
2. 配置**解锁**组件参数，如下图所示。

   ![解锁组件示例](https://docimages.blob.core.chinacloudapi.cn/images/Activities/unlock20201216.png)

   　- 用户名：输入本地电脑的帐户名。
   　- 密码：输入本地电脑的密码。

3. 保存流程退出编辑器。
4. 以管理员身份运行编辑器。

   ![管理员运行编辑器](https://docimages.blob.core.chinacloudapi.cn/images/Activities/adminrun20201216.png)

5. 在编辑器中单击“工具 > Windows屏幕解锁服务”  进行安装Windows屏幕解锁服务。

    ![Windows解锁服务](https://docimages.blob.core.chinacloudapi.cn/images/Activities/windowsunlockservice20201216.png)

6. 打开刚刚创建的项目流程并运行，可实现自动解锁已锁的屏幕，如下图所示。

    ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/unlockresult20201216.gif)  