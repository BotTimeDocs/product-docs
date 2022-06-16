# RPA常见问题

[toc]

## 一、安装、激活&登录

### FAQ：安装编辑器或机器人的硬件和软件要求是什么？

<font color=5a6877> 【解决方法A1_00001】
在安装编辑器或机器人之前，建议您先查看[硬件和软件要求](待补充)。为了避免安装失败，建议安装时：
* 关闭杀毒软件
* 使用管理员权限安装

 </font></br></br>
 ---
 </br>

### FAQ：使用许可证本地激活编辑器/机器人时，报错：“该许可证不能在当前计算机上注册。”
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A1_00001.png)
<font color=5a6877> 【解决方法A1_00002】:
1. 确认是否为云扩商务提供的正确有效的许可证。
2. 如果许可证过期或无效
    * **过期时：**请在云扩控制台的“管理中心 > 许可证管理”中重新申请许可证。
    * **无效时：**将许可证复制粘贴至记事本中，确认是否有多余的空格导致，尤其是许可证字符串的开头或结尾处。

 </font></br></br>
---
</br>

### FAQ：使用控制台账号登录机器人时，报错：“连接字符串无效”。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A1_00001-1.png)

<font color=5a6877> 【解决方法A1_00003】:
1. 确认登录界面上的连接字符串是否为控制台首页中的连接字符串。
2. 如果不是控制台首页中的连接字符串，而是“控制台 > 机器人管理” 中连接机器人的字符串，则需重新复制控制台首页中的连接字符串并使用正确的控制台账号登录。
 </font></br></br>
---
</br>

### FAQ：机器人控制台激活时，提示：机器人内部异常，请稍后重试

<font color=5a6877> 【解决方法A1_00004】:情况排查：
已知两个情况：
1. 机器人要求使用的是控制台首页连接字符串，填错成了控制台机器人详情的连接字符串
2. 控制台部署不完整，没有启用websocket支持
备注：其它情况需要研发介入

 </font></br></br>
---
</br>

## 二、插件/扩展

### FAQ：安装扩展时已经关闭所有浏览器窗口，但仍提示关闭浏览器
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/2-1.png)

<font color=5a6877> 【解决方法A2_00001】:出现该提示时可打开“任务管理器”找到提示的浏览器进程，选中后点击“结束任务”之后重新安装浏览器扩展即可。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/2-2.png)

 </font></br></br>
 ---
 </br>

### FAQ：Chrome 录制失败，无法与 Chrome 扩展通信？
<font color=5a6877> 【解决方法A2_00002】:若出现无法与浏览器扩展通讯的提示，可按照如下步骤排查：
1. 检查 chrome 浏览器扩展，是否安装了 chrome 扩展并且启用，如果未安装“云扩录制器”扩展，需要 通过 Studio 进行自动安装。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/3-1.png)

2. 当打开 chrome 后，检查“任务管理器”中是否存在 EncooNativeMessageHost.exe 进程：，该进程是 RPA 与 chrome 浏览器的通信进程，如果不存在，则检查(1)。

**<说明>**
* 如果 EncooNativeMessageHost.exe 进程未启动，需暂时关闭杀毒软件的防护功能，然后 通过 Studio 进行自动安装。
* 如果 EncooNativeMessageHost.exe 进程未启动且已经关闭杀毒软件并安装了扩展，需暂时关闭杀毒软件的防护功能并删除“C:\Users\当前用户\AppData\Local\Encoo\messagehost”文件夹，然后再次通过 Studio 进行安装扩展。
* 如果杀毒软件暂时无法关闭，需要公司超级管理员授权才可关闭时，请用可修改注册表的用户登录，手动修改注册表，手动安装 Chrome 扩展。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/3-2.png)

 </font></br></br>
---
</br>


## 三、流程开发

### FAQ：无法识别到指定的元素，怎么办？
<font color=5a6877> 【解决方法A_300001】:
1. 匹配超时的时间设置长一点
2. 录制时按F4切换录制技术，直至可以识别为止
3. 如果以上无法解决，录制时按Ctrl+框选的形式，使用图像识别
4. 如果以上无法解决，尝试更换组件，如，“坐标点击”、“CV类组件”
5. 如果以上无法解决，借助元素探测器，找到元素值，观察其特征，如果目标 title 为动态的
❖ 把动态字段的值用`*`通配符来代替
❖ 使用{{变量名}}基础变量来代替
6.  如果以上无法解决， 勾选生成 选择器编辑器右上角的XPath（仅支持 WEB），使用XPath代码，如，//label[@for='confCode']/..//input[contains(@placeholder,'变量代码')]，然后重新指向元素

 </font></br></br>
---
</br>

### FAQ：用循环重复做同样的操作获取网页结构化数据，为何每次获取的数据都缺少一列？
<font color=5a6877> 【解决方法A_300002】:
1. 排查缺少的那一列的网页结构是不是table元素。如果Table的td标签再套Div，然后Div里面再有span，有可能识别不到
2. 需要再获取一次结构化数据，在“是否需要导入全部”时，选择“否”，再选择下一行数据，然后再循环两次结构化数据获取的Datatable整合为一个。

 </font></br></br>
---
</br>

### FAQ：如何使用用友U8获取结构化数据？
<font color=5a6877> 【解决方法A_300003】:检查识别的录制技术：
❖ 如果录制技术为JAB时可识别，则可以使用该录制技术进行获取结构化数据
❖ 如果录制技术为UIA时可识别，则需要用市场组件【FlexGrid表格抓取】来获取数据

 </font></br></br>
 ---
 </br>

### FAQ：如何获取表格内的其他属性，比如Web文本上的超链接？
<font color=5a6877> 【解决方法A_300004】:在指定数据源后的弹窗中点击“新增”按钮，在下拉框中选择“Href”属性即可获取到文本上的超链接，此外还可以通过该方法获取Title甚至一些自定义属性：
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/4-1.png)


获取成功后如图：
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/5-1.png)

 </font></br></br>
 ---
 </br>

### FAQ：指定元素时报错“无法识别您所指定元素的规律，无法获取……”该如何处理？
<font color=5a6877> 【解决方法A_300005】:提示该错误是因为指定的第二个元素与第一个元素间不存在可以获取数据的规律，需要重新指定一个有规律的元素才能成功运行。首先需要确保指定的两个元素要在同一个页面、同一个域下，其次要保证指定的两个元素有一定的相似点，通常元素归属于同一个父节点下的同类型节点或节点属性都可匹配，具体的信息可以按F12来查看浏览器的源代码来查找可以匹配的元素。

 </font></br></br>
 ---
 </br>

### FAQ：指定元素成功，但获取到的表格为空是什么原因？
<font color=5a6877> 【解决方法A_300006】:获取结构化数据会优先识别表格，而指定的这个表是空的，页面显示的数据未存在这个表格内，所以获取到的表就是空的。遇到这种情况可以按F12来查看并指定实际显示数据的表的位置，或者在弹出是否获取整表时点击“取消”，之后根据提示手动指定行列中的数据来逐列获取数据即可。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/5-2.png)
 
 </font></br></br>
 ---
 </br>



### FAQ：删除失败或写入组件失败，一直卡在删除或写入组件
<font color=5a6877> 【解决办法A_300007】：去掉保护

 </font></br></br>
 ---
 </br>

### FAQ：写入公式,单元格的格式是文本(其实是带了'),导致需要双击下单元格确认格式才能生效

<font color=5a6877> 【解决办法A_300008】：可以先设置格式在插入,或者把插入的那一列改为数值格式,或者用执行宏

 </font></br></br>
 ---
 </br>

### FAQ：写入区域卡死
<font color=5a6877> 【解决办法A_300009】:某些数据含有特殊字符,比如CSV转excel的情况下


 </font></br></br>
 ---
 </br>

### FAQ：Excel/WPS组件：读取单元格内容，出现换行？
<font color=5a6877> 【解决办法A_300010】:str.Trim('\n')

 </font></br></br>
 ---
 </br>

### FAQ：Excel/WPS组件：写入单元格怎么换行？
<font color=5a6877> 【解决办法A_300011】:写入内容输入 +'\n' 就可以换行了

 </font></br></br>
 ---
 </br>

### FAQ：Excel/WPS组件：如何取消工作表密码保护

<font color=5a6877> 【解决办法A_300012】:如下所示
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/7-1.png)

 </font></br></br>
 ---
 </br>
 
### FAQ：Excel/WPS组件：如何关闭数据链接更新提示弹窗？

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/7-2.png)
<font color=5a6877> 【解决办法A_300013】: 选择 Excel选项>> 高级>> 常规>>请求自动更新
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/7-3.png)![](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/8-1.png)
 </font></br></br>
 ---
 </br>

### FAQ：Chrome打印页面元素验证失败，如何处理？
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/8-2.png)
直接指定上图中的元素后进行验证就会验证失败，这是由于该应用窗口在没有焦点的时候拿到的进程名与有焦点时不一样，录制时焦点不在该窗口上而运行时焦点在该窗口上，所以验证运行就会失败。该问题在Chrome的弹窗、Chrome打印页面或金蝶K3等窗口比较常见。

<font color=5a6877> 【解决办法A_300014】:在组件进入录制状态后先按F2，在暂停倒计时时手动点击金蝶K3或Chrome的窗口，这样就会让该软件窗口处于获得焦点的状态，然后等到5秒延迟结束后再录制抓取对应元素即可。运行流程时焦点会自动保持在最新打开的窗口上，按照上述步骤录制的流程就可以正确运行。

 </font></br></br>
 ---
 </br>

### FAQ：使用鼠标系列组件拖动窗口滚动条时无法定位或运行成功但未成功滚动，如何处理？
<font color=5a6877> 【解决办法A_300015】:上述场景不建议使用“鼠标拖动”操作滚动条来运行。</br>
* 桌面应用可以使用组件“鼠标滚动(中键)”、使用“点击”组件点击滚动条的上下按钮或是“发送快捷键”的“{PGDN}”来更好的实现；
* Web页面不需要滚动页面，直接指定要操作的滚动后才显示的元素即可，在运行时会自动定位。</br>
如果确需使用鼠标拖动组件操作滚动条，则需注意指定的滚动条滑块的位置，即图中框起来的区域：</br>
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/9-1.png)

之后设置属性“纵坐标偏移”多少像素才能正确触发滚动操作：
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/9-2.png)

如果指定到的是整个滚动条或滚动条上非滑块的区域就会出现组件运行成功但页面未滚动的现象。

 </font></br></br>
 ---
 </br>

### FAQ：鼠标拖动成功但滚动条只滚动了一点，是怎么回事？
<font color=5a6877> 【解决办法A_300016】:拖动只运行一点可能是因为设置的偏移属性太小，也可能是窗口未全屏导致的，可将要执行拖动的窗口全屏后，再设置大一些的值(如1000像素)即可成功运行。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/9-2.png)
 </font></br></br>
 ---
 </br>

### FAQ：输入文本时被输入法拦截导致输入内容发送变化，怎么办？
​<font color=5a6877> 【解决办法A_300017】:因为“模拟键盘”是触发key的事件来输入文本的，所以会被系统输入法所阻挡，如果需要以“模拟键盘”的方式输入文本就需要将系统的默认输入法设置为系统自带的“英语(美国) – 美式键盘”，以Win10为例：进入系统设置->打开“时间和语言”->点击“语言”->打开“键盘”，将“替代默认输入法”的选项修改为“英语(美国) – 美式键盘”
​![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/10-1.png)
 ​</font></br></br>
 ---
 </br>

### FAQ：输入文本组件：运行成功但文本未被成功输入，如何解决？
<font color=5a6877> 【解决办法A_300018】:运行成功是因为组件找到了元素，并根据设置发送了事件，未成功输入说明发送的事件文本未显示到输入框内，可能是指定错了元素或者元素不支持设置焦点。所以首先判断一下指定的元素是否有误，即确保该组件指定的元素是要输入的文本输入框而不是输入框所在的DIV或窗体；在确认无误后可以将“输入方式”改为“模拟键盘”：
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/10-2.png)
如仍未输入成功可将“输入前行为”改为“点击”：
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/10-3.png)
 </font></br></br>
 ---
 </br>

### FAQ：输入文本组件：提示“元素无法输入文本”或不能指定的元素时如何处理？
<font color=5a6877> 【解决办法A_300019】:“输入文本”支持“input”类型的元素，指定非该类型的元素时就会跳出该提示，解决办法是在“输入文本”前添加一个“点击”组件，点击需要输入文本的元素，之后“输入文本”组件不指定元素，将文本填入即可：
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/11-1.png)

或是使用“发送快捷键”、“设置剪贴板”等组件操作。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/11-2.png)
 </font></br></br>
 ---
 </br>

### FAQ：自动化过程中提示需要“管理员权限”时如何处理？
<font color=5a6877> 【解决办法A_300020】:：Windows下操作很多应用时需要更高级别的应用时需要管理员权限才能做到，比如任务管理器，资源监视器等。要录制、运行这些应用时，需要右键项目名词，之后点击“项目设置”

在弹出的窗口中找到 常规->执行权限->选择“以管理员权限运行”
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/12-1.png)
之后关闭编辑器，在编辑器上右键，选择“以管理员身份运行”即可：
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/12-2.png)

 </font></br></br>
 ---
 </br>

## 四、流程调试

## 五、流程运行

### FAQ：机器人运行时黑屏，如何排查与解决？
机器人开启录屏执行流程，流程结束后，本地或控制台上看到的录屏视频画面是黑屏，但视频里面还是有字幕的。
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/13-1.png)
<font color=5a6877> 【解决方法A5_00001】:
* 如果已使用mstsc远程桌面连接到了该机器人环境，并且mstsc没有断开，而是将窗口最小化了。只需断掉mstsc或保持mstsc窗口不被最小化即可
* 如果在流程执行前、或执行过程中，通过RDP会话保持功能，使当前session进入了“远程连接已断开，但session仍在活动中”的状态。但此时因为一些客户的环境设置了“自动锁屏”，使得当前session进入了锁屏状态，也就无法录制到任何画面了。即, 出现此类问题时，运行环境满足以下几个特点：
    ○ 机器人所在的环境是通过远程桌面访问的
    ○ 机器人开启了RDP会话保持
    ○ 计算机开启了“自动锁屏”，并且已进入锁屏状态

根据如下方法进行排查：
**方法一：修改本地安全策略**
1. 进入secpol.msc，找到如图设置并双击

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/13-2.png)

2. 删除下图中的数值（即不锁屏），点击确定

![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/14-1.png)
  
**方法二：修改注册表**
1. 打开regedit，`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System`
2. 如果需要设置为不锁屏，删掉"InactivityTimeoutSecs"项目，或是将该项目的值改为0
3. 如果需要保留锁屏但要延长自动锁屏时间，若"InactivityTimeoutSecs"已存在，则直接将值修改为新的自动锁屏时间；否则可以在右侧创建一个名为"InactivityTimeoutSecs"的DWORD(32位)项目，值为自动锁屏时间

 </font></br></br>
 ---
 </br>

## 六、流程管理

## 七、私有化部署

### FAQ：如何清理私有化部署中的日志文件？

<font color=5a6877> 【解决方法A7_00001】:如果控制台的系统设置中没有流程日志清理功能，可升级至最新版控制台。如暂时无法升级，但日志文件过大，可手动执行以下脚本处理：
cd  {控制台安装目录} #例如在/usr/console/consolev4pvt-4.1.118351
rm -rf data/minio/.minio.sys/multipart/*
rm -rf data/minio/.minio.sys/tmp/*
rm -rf data/minio/v2-robot*

控制台目录结构
![-w400](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/15-1.png)

 </font></br></br>
 ---
 </br>

