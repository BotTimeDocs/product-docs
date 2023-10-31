# FAQ5：流程运行与维护

<br>

#### Q：控制台许可导入了新的授权，发现机器人重新登录账号激活之前的机器人不能用的可能原因是什么？

<br>


<font color=5a6877>
<br><br>

**【解决办法-A6_00010】**: 

* 若状态“未占用” >> 确认许可证情况，如果是用的固定许可证，固定许可证需要先占用许可，才可以使用。如果当前不占用可能是旧的许可过去了，请先撤销占用的就许可之后分配新许可使用;
* 若链接状态“空闲” >> 说明已有电脑登录了这俩机器人，那这两个机器人则肯定不能被选择

</font>
<br><br>
---
<br> 

#### Q：编辑器如何读取Excel中的空白单元格，空值如何判断？

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633097533575.jpg"/>

<br>


<font color=5a6877>
<br><br>

**【解决办法-A5_00025】**: 见如下流程示例

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633097640019.jpg"/>

</font>
<br><br>
---
<br> 

#### Q：为何机器人执行日志的录屏经常会出现白屏的情况？

<br>

<font color=5a6877>
<br><br>

**【解决办法-A6_00009】**:关掉chrome的硬件加速。新版chrome在云虚拟机上开了硬件加速会有一定几率出现白屏 环境问题和rpa无关

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16633095948060.jpg"/>
 
</font>
<br><br>
---
<br> 

#### Q：如果已购买云扩控制平台以及机器人，如果需要扩容机器人，可以从原有控制台授权新增。还是需要重新申请控制台以及机器人？

<br>


<font color=5a6877>
<br><br>

**【解决办法-A6_00008】**:
后面新的版本可以直接覆盖的，太老的控制台版本不行 像这种旧的界面 就不支持直接覆盖

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16632970274374.jpg"/>

</font>
<br><br>
---
<br> 

 #### Q：社区版编辑器，会默认使用最新版本的市场流程组件吗？

<br>

<font color=5a6877>
<br><br>

**【解决办法-A6_00007】**: 以超级鹰组件为例，社区版是强制勾选的，编辑器不能去掉“总是使用最新”的勾选

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/09/16/16632963660671.jpg"/>

</font>
<br><br>
---
<br> 
 
 
#### Q：控制台激活的机器人运行需要网络的样子，如果运行过程中机器人的网络中断了，对当前任务的运行和后续任务的下发会有什么影响？

<br>


<font color=5a6877>
<br><br>

**【解决办法-A6_00006】**:

* 运行过程中机器人的网络中断了，不影响任务执行，但执行完成后执行结果和录屏无法上传到控制台，得重新连接后才会上传到控制台；

* 机器人处于"断开"的情况下，后续下发的任务且任务（流程部署）配置为"无可用机器人时：等待"，在机器人重新连接后会按下发顺序执行"等待"状态的任务。

</font>
<br><br>
---
<br> 

#### Q：目前是机器人固定许可证，怎么弄成浮动的

<br>

<font color=5a6877>
<br><br>

**【解决办法-A6_00005】**:

控制台-RPA中心-机器人管理，在机器人的基本信息处可以更改

退出登录 之后 进去对应界面 可以重新下，前提是要有对应浮动许可
    
</font>
<br><br>
---
<br> 
 
 


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
