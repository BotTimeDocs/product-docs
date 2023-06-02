# 如何在远程桌面最小化时运行流程

## 现象
当远程桌面最小化时执行部分流程会运行失败，这是因为Windows内置的mstsc远程工具在断开或最小化时会停止渲染桌面元素，可以理解为锁屏，流程中的自动化组件无法获取到桌面元素，自然就会失败。

## 解决方案

### 方法1：流程中避免使用自动化组件

包括但不限于高级自动化中的带有选择器、需要指定元素的组件。这些组件依赖于桌面元素，不使用这些组件流程就可以正确运行。

### 方法2：使用第三方远程桌面应用

如Teamviewer、向日葵等，这些应用在最小化后仍保持渲染桌面元素，可以支持自动化组件正确运行。

### 方法3：使用跳板机

可以在远程桌面A中连接远程桌面B,之后最小化远程桌面A，此时远程桌面B不会受到影响，可以在远程桌面B中正确运行自动化流程。

### 方法4：修改注册表

1. 关闭本地全部远程桌面；

2. 按快捷键 ```Win+R``` 呼出运行窗口，在窗口中输入 ```regedit``` ，点击确定后进入注册表编辑器：

    <img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202005270001.png"/>

3. 进入如下注册表项：

    32位系统： ```HKEY_LOCAL_MACHINE\Software\Microsoft\Terminal Server Client```

    64位系统： ```HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Terminal Server Client```

4. 右键“Terminal Server Client”文件夹新建一个“选择DWORD(32位)值”

    <img src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202005270002.png"/>

5. 双击修改该值，数值名称改为```RemoteDesktop_SuppressWhenMinimized``` ，数值数据修改为 ```2``` 点击确定保存

    <img src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/202005270003.png"/>

6. 关闭注册表后重启远程桌面，即可在最小化远程桌面时正确运行自动化流程。