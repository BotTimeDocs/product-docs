# 解锁

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/Unlock.mp4"></video>

## 概述

解锁系统屏幕，进入系统桌面。

>**说明：**
>
>运行此组件前，需安装 [Windows 屏幕解锁服务](../../../Studio/Extensions/WindowsUnlockService.md)扩展。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **用户名**：登录系统的用户名或微软帐户。
- **密码**：登录系统的密码（微软帐户需要输入微软帐户的密码）。

### 可选项

- **超时**：超时时间，默认超时10s，可自定义调整。

## 使用示例

**前置必要组件**：[锁屏](../Screen/WindowsLockActivity.md)

**此流程执行逻辑**：将已锁屏的计算机解锁。

![解锁组件示例](https://docimages.blob.core.chinacloudapi.cn/images/Activities/unlock20201216.png)

## 常见问题

**1.账户注销后无法解锁**
解锁支持对登陆账号后的锁屏进行解锁，账户未登录时无法触发这个操作，所以是不支持的。如果想解锁这种场景，登录账号之后锁屏就可以解锁了。

