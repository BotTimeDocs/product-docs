# 指南七《Windows远程桌面专题(企业版)》

<br>

>导读: 
> 
> * 重在带大家了解什么是远程桌面扩展？
> * (使用前)安装准备工作：安装Windows远程桌面扩展、Java扩展、浏览器扩展；
> * 远程具体操作：编辑流程、元素录制；
> * 如何卸载远程桌面扩展及远程桌面一般常见问题。
> 

<br><br>

## 一、什么是远程桌面扩展？
远程桌面协议（RDP）是一种通过网络连接到其他计算机的常用方法。借助原生 RDP 自动化，您可以像在自己的计算机上一样生成选择器，并可在网络中的其他计算机上执行这些选择器的操作，而不必为其安装 RPA编辑器或机器人。
</br></br>

## 二、(使用前)安装准备工作

### （1）安装Windows远程桌面扩展
远程桌面支持的系统版本与编辑器一致，推荐使用Windows 10，详情可见[软硬件要求](https://academy.encoo.com/zh-cn/wiki/Studio/quickStart/HarewareAndSoftwareRequirements.md)
</br>

**第一步：** 在确认系统支持后，需要在编辑器所在的本地PC安装远程桌面扩展，安装前先退出本地所有的远程桌面连接，之后进入 开始->工具->点击“Windows远程桌面扩展”：
</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm001.png"/>


</br></br></br>

**第二步：** 根据提示点击确定后即可完成安装：</br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm002.png"/>


</br></br></br>

**第三步：** 之后进入“帮助”查看并记录本地安装的编辑器版本号：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm003.png"/>


</br></br></br>

**第四步：** 将该版本号提供给云扩工作人员以获取远程桌面安装的扩展包：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm004.png"/>

</br>

**第五步：** 将远程桌面扩展包复制到要控制的远程桌面上安装，等待安装后完成后会自动退出安装流程：</br>


<img width = '200'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm005.png"/>


</br></br>

**第六步：** 安装扩展后进入远程桌面的“设置”->“电源和睡眠”中，将屏幕设置为从不休眠：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm006.png"/>


</br></br></br>


**第七步：** 安装完成后退出远程桌面连接，之后重新连接该远程桌面，即可进行自动化操作。
</br>


### （2）安装Java扩展 ——对Java应用进行自动化
同本地Java自动化一样，远程桌面自动化Java应用前也需要安装扩展，步骤如下：
</br></br> 

**第一步：** 找到 RemoteRuntime 安装目录下的 Java 扩展安装程序(EncooJavaExtensionInstaller.exe)，路径为："C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\EncooJavaExtensionInstaller.exe"

</br></br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm008.png"/>

 
</br></br></br>

**第二步：** 以**管理员权限**打开命令行，执行命令：
</br>
`cd C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\`
</br>
切换到安装程序所在目录</br></br>
 ![cmd-Java](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm009.png)
</br>

**第三步：** 执行以下命令执行安装：
</br> 
`EncooJavaExtensionInstaller.exe -install -a`
</br></br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0010.png"/>


</br>
完成安装后即可自动化Java应用程序。
</br></br></br>

>**提示：** 远程桌面安装新的Java应用后需要重新安装Java扩展

</br></br></br>

### (3) 安装浏览器扩展——进行网页自动化

</br>如需对远程桌面网页进行自动化，需要先安装对应的浏览器扩展：
</br>

**第一步：** 找到 Remote Runtime 安装目录下的 Web 扩展安装程序(Encoo.Web.ExtensionInstall.exe)，路径为：
</br>
`C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\Encoo.Web.ExtensionInstall.exe`
</br>

**第二步：** 打开命令行，执行如下命令以切换到安装程序所在目录：
</br>
`cd C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\`
</br>

**第三步：** 根据需要安装的浏览器扩展，执行下方命令执行安装：
</br>

  (1) Chrome 浏览器 `Encoo.Web.ExtensionInstall.exe -install -t Chrome -l zh-CN`</br>
  (2) FireFox 浏览器 `Encoo.Web.ExtensionInstall.exe -install -t FireFox -l zh-CN`</br>
 (3)  360se 浏览器 `Encoo.Web.ExtensionInstall.exe -install -t Web360 -l zh-CN`</br>
  (4) Microsoft Edge 浏览器 `Encoo.Web.ExtensionInstall.exe -install -t Edge -l zh-CN`
</br>

这里以Chrome为例：
</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0011.png"/>


</br></br></br>

**第四步：** 执行命令后会弹出安装扩展的窗口，关闭Chrome后点击“确定”即可完成安装：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0012.png"/>

</br>

</br></br>**第五步：** 安装完成后进入启动Chrome浏览器，点击提示中的“启用扩展程序”：</br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0013.png"/>


</br>

或依次点击“设置”->“更多工具”->“扩展程序”，找到“云扩录制器”扩展启用即可：</br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0014.png"/>

</br> 

启用扩展后重启浏览器，即可进行自动化操作。
</br></br>

## 三、远程具体操作

### (1)编辑流程

远程桌面的流程与本地的流程基本一致，区别是远程桌面的自动化组件需放在“绑定远程桌面窗口”的组件内，才能对远程桌面生效。</br></br></br>

**第1步：** 首先添加一个“绑定远程桌面”的组件，点击“指定窗口”，进入录制状态后指定一个需要远程操作的远程桌面：</br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0015.png"/>

</br></br></br>

**第2步：** 指定完成后组件上会显示远程桌面的缩略图，选择器中也会更新该窗口的信息：
</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0016.png"/>


</br></br></br>

**第3步：** 之后在“绑定远程桌面”组件中添加界面自动化的组件，如“点击”、“输入文本”等，之后录制即可自动化操作远程桌面：
</br>


<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0017.png"/>


</br>

>绑定远程桌面中仅支持界面自动化组件进行录制操作，不支持直接使用Excel或文件组件直接操作，使用非界面自动化组件均会在本地计算机上运行

</br></br>

### (2) 录制
远程桌面的元素选择器与本地桌面端基本一致，点击自动化组件上的“指定元素”按钮，之后直接指定远程桌面中需要录制的元素即可。

当扩展配置生效之后，指定元素时可以选取录制远程桌面中高亮的元素：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0018.png"/>


</br>

</br></br>点击鼠标左键完成录制后可查看选择器，与本地选择器的区别在于在第一级节点上增加了一个“RemoteMetaData”属性，用于记录需要绑定的远程桌面的信息：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0019.png"/>


</br>

</br></br>验证元素时不会自动将远程桌面窗口拉至前台，建议手动将远程桌面切换至前台，以便获得更好的元素验证体验：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0020.png"/>


</br>

运行或发布等功能均与其他流程一致。
</br>

>需注意远程桌面与本地元素不互通，本地录制的组件无法在远程桌面直接使用，须在远程桌面扩展重新录制后才能正常使用</br>

</br></br>

## 四、卸载远程桌面扩展
卸载本地 Windows远程桌面扩展 在本地计算机的注册表中，找到注册表值`HKEY_CURRENT_USER\Software\Microsoft\Terminal Server Client\Default\AddIns\EncooRemotePluginRdp`，删除后重启连接即可。
</br>

卸载Windows远程桌面扩展需进入“控制面板”的“程序和功能”中，找到 “Encoo RemoteRuntime”，右键点击，之后点击“卸载”即可：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/yczm0021.png"/>


</br></br>

## 五、常见问题
1. **录制远程桌面操作时与录制本地操作有什么区别**</br> 
   没有区别，与录制本地操作一致。</br>

2. **是否支持向远程桌面发送文本和快捷键**</br> 
   支持，使用“输入文本”和“发送快捷键”即可</br>

3. **无法录制VM ware的远程桌面操作**</br> 
   暂不支持VM ware应用。</br>

4. **安装好扩展后仍无法录制**</br> 
   重启远程桌面机后即可恢复。如仍不能录制则需要检查本地和远程桌面安装的扩展版本。是否一致，需确保版本一致才能录制。</br>

5. **无法向远程桌面复制文件**</br> 
   远程桌面录制仅支持界面自动化的操作，其他的组件所操作的仍是本地的PC文件，尚不支持直接向远程桌面复制文件。如需文件操作可通过控制台组件或其他方式进行操作。</br>

6. **无法录制远程桌面中的远程桌面元素**</br> 
   当前不支持在已连接的远程桌面中再连接其他远程桌面。</br>
