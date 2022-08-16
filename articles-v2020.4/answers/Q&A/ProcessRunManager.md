# FAQ5：流程运行与维护

#### Q：机器人运行时黑屏，如何排查与解决？

<br>

机器人开启录屏执行流程，流程结束后，本地或控制台上看到的录屏视频画面是黑屏，但视频里面还是有字幕的。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/13-1.png"/>

 <br> <br> <br>

<font color=5a6877> 【解决方法A6_00001】:

* 如果已使用mstsc远程桌面连接到了该机器人环境，并且mstsc没有断开，而是将窗口最小化了。只需断掉mstsc或保持mstsc窗口不被最小化即可
* 如果在流程执行前、或执行过程中，通过RDP会话保持功能，使当前session进入了“远程连接已断开，但session仍在活动中”的状态。但此时因为一些客户的环境设置了“自动锁屏”，使得当前session进入了锁屏状态，也就无法录制到任何画面了。即, 出现此类问题时，运行环境满足以下几个特点：
    ○ 机器人所在的环境是通过远程桌面访问的
    ○ 机器人开启了RDP会话保持
    ○ 计算机开启了“自动锁屏”，并且已进入锁屏状态

<br>

根据如下方法进行排查：

<br>

**方法一：修改本地安全策略**

* Step1、进入secpol.msc，找到如图设置并双击

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/13-2.png"/>


<br>

* Step2、删除下图中的数值（即不锁屏），点击确定

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/14-1.png"/>


<br><br>

**方法二：修改注册表**

<br>

* Step1、打开regedit，`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System`

* Step2、如果需要设置为不锁屏，删掉"InactivityTimeoutSecs"项目，或是将该项目的值改为0

* Step3、如果需要保留锁屏但要延长自动锁屏时间，若"InactivityTimeoutSecs"已存在，则直接将值修改为新的自动锁屏时间；否则可以在右侧创建一个名为"InactivityTimeoutSecs"的DWORD(32位)项目，值为自动锁屏时间

 </font><br><br>
 ---
 <br>

#### Q：日志文件 可以更改存放路径吗 ？

<br>

<font color=5a6877> 【解决方法A6_00002】: 目前暂不支持



 </font><br><br>
 ---
 <br>

#### Q：机器人的流程视频日志存放路径是什么？

<br>

<font color=5a6877> 

【解决方法A6_00003】: 
`%localappdata%\Encoo\Encoo Robot\JobLogs\local\{流程包名}\{版本号} `目录下的所有文件夹，取文件名最大的那个文件夹，视频会在这个目录里


 </font><br><br>
 ---
 <br>

#### Q：控制台视频文件显示上传完成，但是视频展示“当前任务无视频记录”

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A6_00004.png"/>

<br><br>

<font color=5a6877> 

【解决方法A6_00004】: 如果机器人版本是2201之前的版本建议升级到2201之后的版本

 </font><br><br>
 ---
 <br>
