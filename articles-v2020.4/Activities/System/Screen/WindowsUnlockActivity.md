# 解锁

## 视频示例

## 概述

解锁系统屏幕，进入系统桌面。

>**说明：**
>
>运行此组件前，需安装 [Windows 屏幕解锁服务](Studio/../../../../Studio/Extensions/WindowsUnlockService.md)扩展。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **超时**：超时时间，默认超时10s，可自定义调整。

### 输入

- **用户名**：登录系统的用户名或微软帐户，可接变量。
- **密码**：登录系统的密码（微软帐户需要输入微软帐户的密码），可接变量。
  
## 使用示例

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
