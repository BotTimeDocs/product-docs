# 机器人录屏时黑屏

## 问题描述

机器人开启录屏执行流程，流程结束后，本地或控制台上看到的录屏视频画面是黑屏，但视频里面还是有字幕的。

![现象](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/black0120220506.png)

## 限制条件

- 机器人执行流程时，执行流程的 windows 用户需要一个可用的 windows session（即对应的 windows 用户处于登录状态）。
- **windows 远程桌面**（下文简称 RDP）连接时，会为登录的 windows 用户创建一个活动状态的 session；断开时，会注销该 session。而机器人提供了对应功能，能在远程断开时，维持该 session 的活动状态。（即 rdp 会话保持）
- **锁屏** 不会影响 session 状态，但会影响到画面截取（即录屏、截图等功能）; 同时在 RDP 断开的情况下，锁屏没有锁屏画面。

## 根本原因

即 Windows 的接口无法获取到画面，可能有以下两种原因：

1. 已使用 mstsc 远程桌面连接到了该机器人环境，并且 mstsc 没有断开，而是将窗口最小化了。
2. 在流程执行前、或执行过程中，用户通过 RDP 会话保持功能，使当前 session 进入了“远程连接已断开，但 session 仍在活动中”的状态。但此时因为一些客户的环境设置了“自动锁屏”，使得当前 session 进入了锁屏状态，也就无法录制到任何画面了。

    即, 出现此类问题时，客户环境满足以下几个特点：
    - 机器人所在的环境是通过远程桌面访问的
    - 机器人开启了 RDP 会话保持
    - 计算机开启了“自动锁屏”，并且已进入锁屏状态

## 解决方法

### 原因 1 的解决办法

如果是原因 1，解决方法很简单，断掉 mstsc 或保持 mstsc 窗口不被最小化即可。

### 原因 2 的解决办法

如果是原因 2，根据如下方法进行排查：
因为远程计算机使用机器人执行流程，rdp 会话保持是必不可少的，所以解决该问题只能要求客户取消机器人环境上的自动锁屏设置

#### 方法一：修改本地安全策略

1. 进入 secpol.msc，找到如图设置并双击

    ![步骤一](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/black0220220506.png)

2. 删除下图中的数值（即不锁屏），点击确定

    ![步骤二](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/black0320220506.png)

#### 方法二：修改注册表

1. 打开 regedit，`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System`
2. 如果需要设置为不锁屏，删掉 "InactivityTimeoutSecs" 项目，或是将该项目的值改为 0
3. 如果需要保留锁屏但要延长自动锁屏时间，若 "InactivityTimeoutSecs" 已存在，则直接将值修改为新的自动锁屏时间；否则可以在右侧创建一个名为 "InactivityTimeoutSecs" 的 DWORD(32 位)项目，值为自动锁屏时间

### 方法三：使用阻止锁屏工具

[阻止锁屏工具](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/PreventScreenLocked.zip)
