# 手机自动化常见问题

## Android手机设备连接类

**1. 小米手机无法正常连接或无法点击屏幕**
<br>解决办法：

在“开发者选项”中将“**允许模拟点击位置**”、“**USB安装**”、“**USB调试(安全设置)**”等选项打开，部分选项的开启可能需要登录MIUI账号（需要插入SIM卡）

![小米手机设置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/xiaomi20210618.png)

**2. 三星手机无法正常连接或无法正常显示屏幕**

![异常现象](https://docimages.blob.core.chinacloudapi.cn/images/Studio/sansung20210618.png)

<br>解决办法：

- 在“开发者选项”中，打开未知来源、取消权限监控。

- 打开“设置 > 显示 > 屏幕分辨率 > 更改屏幕分辨率”，更改为“WQHD”

![更改屏幕分辨率](https://docimages.blob.core.chinacloudapi.cn/images/Studio/sanscreen20210618.png)

**3. 华为手机无法正常连接**
<br>解决办法：

step1：在输入法设置中，取消安全输入

step2：将“开发者选项 > 监控ADB安装应用”设置为“不勾选”状态

step3：将“开发者选项 > 仅充电模式下允许调试”设置为“勾选”状态

step4：将“应用 > 权限管理 > 设置 > 权限推荐”设置为“勾选”状态

>**说明：**
>
>部分华为型号的手机，可能出现点击位置与实际位置不符的情况（mate20pro, mate7等），需要在"设置 > 显示 > 屏幕分辨率"中，将分辨率设置为最高即可。

**4. OPPO手机无法正常连接**

解决办法：

在“开发者选项”的最底部，勾选“禁止监控权限”

>**说明：**
>
>部分OPPO机型在“开发者选项”下启用USB调试模式，如果10分钟内没有进行开发者模式操作，会主动断开USB模式，需要手动重新开启开发者选项的USB调试模式。

## Android服务端类

**1. 已安装的安卓服务包中pocoservice.apk应用不见了怎么办？**
<br>解决办法：

在运行pocoservice.apk应用前，将其权限调前，且需设置“允许后台运行”、“省电模式移除”等。

**2. 服务运行时使用了VPN，服务中断，怎么处理？**
<br>解决办法：

使用VPN工具时，将本地PC地址设置为“不经过代理”。

![不经过代理的地址列表](https://docimages.blob.core.chinacloudapi.cn/images/Studio/proxy20210618.png)

**3. 在流程录制过程中，鼠标移动没有定位框，是什么原因？**
<br>解决办法：

手动打开移动设备中的pocoservice软件，提示“正在运行”即可。

**4. 是否支持手机设备在运行流程时，使用WIFI连接网络？**
<br>解决办法：

目前暂不支持手机设备WIFI连接运行流程的方式。








## Android手机自动化组件类


发送文本、获取文本、清空文本等

部分OPPO机型在初始化Poco时，或者调用 text() 接口时，会失败报错，
原因可能是因为安装或者切换Yosemite输入法失败（需要输入OPPO账号密码才能切换）。
此时可以先到系统"设置 > 输入法设置"中，将Yosemite输入法设置为默认输入法，如果尚未安装Yosemite输入法，可以在Encoo.Android.Automation同级目录apk文件夹下找到它Yosemite.apk并且手工安装到手机上之后，即可开始使用Poco功能以及 text() 接口。

## Android模拟器运行类

## Android真机运行类

