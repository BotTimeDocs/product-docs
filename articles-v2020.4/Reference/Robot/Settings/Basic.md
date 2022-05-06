# 基本

![基本设置界面](https://docimages.blob.core.chinacloudapi.cn/images/Robot/robotbasic20211231.png)

## 基本设置

- **启动设置**：设置是否默认开机启动。
- **执行流程**：

    - 执行流程时界面最小化：设置执行流程时，机器人界面是否最小化。
    - 执行流程时显示当前执行节点：勾选后，在“正在执行”页显示当前执行节点，并在桌面右下角托盘中显示。
    - 执行流程时自动解锁屏幕：当执行流程时检测到锁屏，机器人将自动解锁屏幕，保证流程正常运行，流程执行结束后再自动锁屏。

- **RDP 远程**：勾选后，当 RDP 远程桌面断开连接时，继续以设定的被远程的计算机的最高分辨率（在被远程的计算机中的“设置 > 显示”中查看“显示分辨率”的最大值），保持会话连接，保证通过定时任务或者控制台下发流程能够正常运行。

  > **说明：**
  >
  > RDP 会话保持需要 Windows 账号具有管理员权限，如果是 Windows Server 系列系统，只能保持一个 Windows 账号 RDP 会话。
  
  判断 RDP 会话是否成功保持连接的方法：
  
  1. 以 windows+R 打开“运行”面板，并输入机器人的日志路径“%LOCALAPPDATA%\Encoo\Log\”
  2. 在文件夹中找到 RdpSessionMaster 开头 log 日志文件，该日志会定时记录 RDP 会话保持下 Windows 状态以及分辨率，如果对应状态是 WTSActive，并且分辨率是在机器人设置分辨率意味着会话保持成功。

## 视频录制

- **保存时间**：支持配置视频文件的保存时间，单位为日。

- **存储容量**：支持配置视频文件的存储限制，单位为 GB 。

## 日志

- **保存时间**：支持配置保留日志文件时间，单位为日。例，机器人设置了日志的保存时间近 3 天，则在设置后的第二天零点生效。

## 控制台

- **控制台**：支持配置是否接受控制台调度。

  > **说明：**
  >
  > 只有企业版在如下情况下，此功能才可用。
  >
  >- 企业版，使用控制台激活。
  >- 企业版，本地激活且在“设置 > 绑定”中已绑定控制台。