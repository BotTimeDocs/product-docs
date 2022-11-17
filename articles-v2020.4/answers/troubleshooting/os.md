# Error7：系统错误

 <br>
 
#### Q：WMI(Windows Management Instrumentation)服务损坏

<font color=5a6877>
<br>

**【解决办法--OS0001】**：修复WMI服务



**方法1**

重建损坏的Windows Management Instrumentation(WMI)服务（**测试通过**）

@echo on </br>
cd /d c:\temp </br>
if not exist %windir%\system32\wbem goto TryInstall </br>
cd /d %windir%\system32\wbem </br>
net stop winmgmt </br>
winmgmt /kill </br>
if exist Rep_bak rd Rep_bak /s /q </br>
rename Repository Rep_bak </br>
for %%i in (*.dll) do RegSvr32 -s %%i </br>
for %%i in (*.exe) do call :FixSrv %%i </br>
for %%i in (*.mof,*.mfl) do Mofcomp %%i </br>
net start winmgmt </br>
goto End </br>

:FixSrv </br>
if /I (%1) == (wbemcntl.exe) goto SkipSrv </br>
if /I (%1) == (wbemtest.exe) goto SkipSrv </br>
if /I (%1) == (mofcomp.exe) goto SkipSrv </br>
%1 /RegServer </br>

:SkipSrv </br>
goto End </br>

:TryInstall </br>
if not exist wmicore.exe goto End </br>
wmicore /s </br>
net start winmgmt </br>
:End </br>

将这段代码保存BAT格式，之后在服务器上运行即可

**方法二**

1. 单击开始，然后右键单击我的电脑。
2. 在快捷菜单上，单击管理。
3. 在计算机管理控制台的左窗格中，双击“服务和应用程序”。
4. 在“服务和应用程序”下，单击服务。
5. 在计算机管理控制台的右窗格中，找到然后右键单击 Windows Management Instrumentation。
6. 在快捷菜单上，单击停止。
7. 启动 Windows 资源管理器，然后找到 %SystemRoot%System32WbemRepository 文件夹。
8. 删除 %SystemRoot%System32WbemRepository 文件夹中的所有文件。
9. 重新启动计算机。重新启动计算机。

> 解决办法转自链接： http://t.zoukankan.com/fromchaos-p-2661646.html

</font>
<br><br>
---
<br>
<br>
 
#### Q：系统未设置MD5支持

<font color=5a6877>
<br>

**【解决办法--OS0002】**：修改注册表

解决方法：

1. 在window中打开功能里输入```regedit```，之后按回车打开注册表编辑器；

2. 进入如下路径中 
```HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa\FipsAlgorithmPolicy ```

将 enable设置为0 即可。 

![os0001](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/os00001.png)

> 解决办法转自链接： https://www.cnblogs.com/527289276qq/p/7001816.html