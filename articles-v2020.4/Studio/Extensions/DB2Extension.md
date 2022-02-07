# IBM DB2 扩展

安装 IBM DB2 扩展来进行 IBM DB2 数据库的自动化。

> **说明：**
>
> 安装好 IBM DB2 扩展后，配合“**连接数据库**”组件进行使用。

## 安装

### 在线安装

1. 以管理员身份运行编辑器或机器人，在编辑器的“**开始 > 工具 > 扩展**”或机器人的“**设置 > 扩展**”中找到“**IBM DB2 扩展**”。
2. 单击“**IBM DB2 扩展**”图标。
3. 在弹出的“**安装 EBM DB2 扩展**”提示框中，单击“确定”按钮，进行安装。
   ![IBM DB2 安装提示](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ibmdb220210105.png)
4. 安装正常，则提示安装成功。
   ![安装成功 ](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tips20210105.png)  
5. 单击“确定”按钮，完成安装。

### 离线安装

1. 在有网络的环境中事先下载 IBM DB2 扩展，如 [ibm.data.db.provider.11.1.4040.4.nupkg](https://share.weiyun.com/NXqMlQJN)
2. 将下载下来的 IBM DB2 扩展的安装包替换至离线编辑器或机器人的安装路径中。

    - 编辑器中的扩展安装路径：`%UserProfile%\AppData\Local\Encoo Studio\app-1.1.2112.6\buildinActivities`
    - 机器人中的扩展安装路径：
`%programfiles(x86)%\Encoo Robot\app-1.1.2112.6\buildinActivities`

3. 以管理员权限运行编辑器或机器人，在编辑器或机器人扩展界面中，单击安装“IBM DB2 扩展”。

## 卸载

1. 找到编辑器或机器人的安装路径。
   > **说明：**
   >
   >- 编辑器的默认安装路径为 `%UserProfile%\AppData\Local\Encoo Studio`。
   >- 机器人的默认安装路径为 `%UserProfile%\AppData\Local\Encoo Studio`。

2. 在该安装路径下的类似 `app-x.x.20xx.xx` 文件夹中找到如下文件夹和文件进行手动删除。
    ![卸载 DB2](https://docimages.blob.core.chinacloudapi.cn/images/Robot/uninstallDB220210114.png)