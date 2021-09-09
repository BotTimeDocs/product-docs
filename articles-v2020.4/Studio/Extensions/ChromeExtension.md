# Chrome 扩展

## 概述

在编辑器或机器人中，你可以通过安装 Chrome 扩展来进行浏览器的自动化。

> **注意：**
>
>- Chrome 版本最低为 60。
>- 在安装该扩展前，可能会要求你关闭 Google Chrome，因此请务必将处理中的相关任务进行保存。

## 自动安装

1. 在编辑器的 **工具 > 扩展** 下你可以看到你需要安装的 Chrome 扩展。

    ![Chrome 扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/extensioninpath20201019.png)

    > **说明：**
    >
    > 在机器人中，Chrome 扩展的路径为 **设置 > 扩展** 下。  

2. 单击“Chrome 扩展”，在弹出的对话框中，单击“确定”。

    ![确定安装 Chrome 扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/chrome-installation.PNG)

3. 打开 Chrome 浏览器，点击侧面导航栏的“更多工具 > 扩展程序”。

    ![打开扩展程序](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/chrome-openExtension.png)

4. 在打开的 <chrome://extensions/> 页面中，找到“云扩录制器”扩展。

5. 点击该扩展右下角的启用按钮。

    ![启用扩展程序](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/chrome-usingExtension.png)

## 手动安装

在部分场景中（如，无法关闭杀毒防护软件）无法自动安装 Chrome 扩展时，可选择手动安装 Chrome 扩展以便完成自动化操作。

1. 在Chrome浏览器中，打开Chrome扩展页面（<chrome://extensions/>）。
2. 进入Studio程序的Chrome扩展所在的文件夹。

    ![Studio程序所在路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/studiopath20210909.png)

    ![chrome扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/chromecrx20210909.png)

3. 拖入"gcpfpefcddakgefbkjlmkooffapfdmbi_main.crx"至浏览器的Chrome扩展页面，添加并启用扩展。

    ![安装chrome扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/addchromecrx20210909.png)

4. 复制chromemessagehost文件夹中的所有文件至“C:\Users\UserName\AppData\Local\Encoo\messagehost\chrome”文件夹中。

    ![chromemessagehost文件夹](https://docimages.blob.core.chinacloudapi.cn/images/Studio/chromemessagehost20210909.png)

    >**说明：**
    >
    > `UserName`为当前系统用户名。

    ![chrome路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/chrome20210909.png)

5. 修改chrome文件夹下“encoorpachromemessage.json”配置文件，将配置文件中的path值修改为同目录下EncooNativeMessageHost.exe文件的绝对地址。

    ![chrome配置文件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/chromepath20210909.png)

6. 使用“Win+R”打开运行窗口并输入`regedit`打开注册表窗口。

    ![运行窗口](https://docimages.blob.core.chinacloudapi.cn/images/Studio/winR20210909.png)

7. 查看注册表的“HKEY_CURRENT_USER\SOFTWARE\Google\Chrome”路径下是否有“NativeMessagingHosts”文件夹。

    >**说明：**
    >
    >如果没有该文件夹，则执行如下步骤：
    >
    >1. 在“Chrome”文件夹上右击，选择“新建 > 项”，新建一个“NativeMessagingHosts”文件夹。
    >2. 在“NativeMessagingHosts”文件夹上右击，选择“新建 > 项”，新建一个“com.bottime.chrome.msghost”项。

    ![NativeMessagingHosts](https://docimages.blob.core.chinacloudapi.cn/images/Studio/regeditchrome20210909.png)

8. 打开“C:\Users\UserName\AppData\Local\Encoo\messagehost\chrome”路径下“encoorpachromemessage.json”配置文件，修改`name`的值为“com.bottime.chrome.msghost”。

    ![name](https://docimages.blob.core.chinacloudapi.cn/images/Studio/chromename20210909.png)

9. 双击注册表“com.bottime.chrome.msghost”项右侧窗口中的“默认”字样，在弹窗的“数值数据”中输入“encoorpachromemessage.json”配置文件的绝对地址。

    ![编辑注册表](https://docimages.blob.core.chinacloudapi.cn/images/Studio/editconfig20210909.png)
