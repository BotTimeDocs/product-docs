1. **Q：** 安装时弹出程序崩溃提示，如图：

   ![安装崩溃](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/installCollapse.png)

   **A：** 打开控制面板->程序->卸载程序，在卸载或更改程序列表中检查是否安装.Net Framework 4.6.1及以上版本的.Net Framework环境。如果未安装，请先下载.Net Framework 4.6.1并安装，安装好之后重启电脑再进行云扩RPA编辑器的安装。下载地址：<https://www.microsoft.com/zh-CN/download/details.aspx?id=49982>

2. **Q:** 点击安装，显示安装失败

   ![安装失败](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/installationFailed.png)

   **A：** 检查当前用户在安装目录的读写权限，如果当前用户在安装路径没有读写权限，则要用管理员账号登录，在安装目录右键，点击属性，点击安全标签，添加目标账户，并添加完全控制权限，最后点击确定，然后退出管理员账号，用目标用户登录进行安装。

3. **Q:** 卸载失败

   **A：** ① 安装目录(Program files x86)，25版本以后的安装目录在用户目录AppData\Local\，下面 encootech文件夹删掉</br>
   ② C:\ProgramData\Package Cache\ 里面搜一下 Digi4th开头的 都删掉</br>
   ③ 删除windows服务 DataBusService(cmd 命令行 sc delete DataBusService)

4. **Q:** 编辑器的默认安装目录是什么？

   **A：** %USERNAME%\AppData\Local\Encootech\Encoo Studio

5. **Q:** 机器人的默认安装目录是什么？

   **A：** %programfiles(x86)%\Encootech\Encoo Robot

6. **Q:** 默认日志路径是什么？

   **A：** %username%\AppData\Local\Encoo\Log。(Installation为安装日志)

7. **Q:** 从市场下载的组件包存放在本地计算机什么目录？

   **A：** %username%.botTimeRPA\packages\Activity

8. **Q:** 如何在没有外网访问的计算机使用组件市场的组件？

   **A：** 打开本地下载好的组件包地址：C:\Users%USERNAME%.botTimeRPA\packages\Activity

   ![本地下载组件地址](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/localActivitiesPosition.png)

   ① 拷贝所需要的包文件夹</br>
   ② 将拷贝的文件夹放至目标电脑同样路径下，没有路径可手动创建</br>
   ③ 用NotePad++或其他文本编辑器打开目标工程文件夹下的botTimeRPA.json文件</br>
   ④ 在botTimeRPA.json文件内修改Dependencies属性添加依赖，以DataTableTools工具包为例：（可以将本地工程该属性直接复制到目标工程文件内。）

   ![添加依赖](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/addDependence.png)

   ⑤ 最后重启或打开编辑器，打开工程即可自动引用市场包。

9. **Q:** Chrome录制失败，自动化失败有哪些原因？

   **A：** ① 检查chrome浏览器扩展，是否安装了chrome插件并且启用，如图：

   ![启用扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/googleExtension.png)

   ② 当打开chrome后，检查任务管理器是否存在进程：EncooNativeMessageHost.exe，该进程是RPA与chrome浏览器的通信进程，如果不存在，则检查①。

   ![检查进程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/taskManager.png)


10. **Q:** 怎么安装chrome插件？

    **A：** 打开编辑器，在窗口上方点击扩展，然后点击chrome扩展，根据提示操作即可。（在安装后，请手动打开浏览器，并打开扩展：chrome://extensions/，启用扩展。）

    ![安装扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/installExtension.png)
