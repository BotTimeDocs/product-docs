# 流程库

机器人可以通过桌面点击的方式执行流程，也可以通过控制台集中管理执行流程。

控制台集中管理执行流程详见：[如何下发一个流程](Console/../../Console/workflow/manageworkflow.md)

本地执行的流程来源分为两种：

1. 本地流程文件文件：通过编辑器导出的流程包（后缀为.dgs的流程压缩包）
2. 控制台流程库:获取机器人所在资源组的[流程包](..\Console\packages\aboutPackages.md)

**控制台流程库**仅供通过控制台激活的机器人使用。

同一机器人同一时间只能执行一个流程，仅在流程执行结束后，方可执行下一个流程。


### 执行本地流程
1. 打开本地流程库
2. 点击导入流程，将编辑器导出的项目文件（*.dgs）导入本地流程库。
3. 选择你想要执行的流程，你可以输入流程名点击搜索进行查询。
4. 点击“执行”时，将会弹窗确认信息。
    
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/flowofexecution20201201.png)
    
 - 流程：显示当前需要执行流程的流程名称和版本号。
 - 参数：若当前流程需要传入参数，点击执行后会弹窗提示输入参数。
   >**说明：**
   >
   >若参数类型为 Encoo.DataType.FilePath、Encoo.DataType.FolderPath 时，可根据参数类型选择文件或文件夹路径，无需手动填写。
 - 选项：各选项参数解释如下表所示：

  
   |  选项    |说明      |
   | :---- | :---- |
   |   录制视频   |是否需要在流程执行过程中录制某种执行状态的视频。|
   |   执行过程截图   |是否需要在流程执行过程中进行截图。<br><font color="grey" size="3" face="楷体"> **说明：**<br>  <ul><li>截图后的图片保存在当前流程日志目录下的 Screenshots 文件夹下。</li><li>图片名称格式：{流程名称}-{截图时间：年月日时分秒}.jpg ,如：小E绘画大师-20201201164102599.jpg </li> </ul> </font>  |
   |   以管理员权限执行   |是否以管理员身份执行，勾选表示以电脑管理员身份运行，否则以普通用户身份执行。      |
   |   超时时间   | 运行时间超过设定的时间时终止流程。如，勾选“超时时间1分钟”，表示需要在1分钟之内执行完成，否则终止流程。|   


5. 点击确认，流程在快速准备后将自动执行。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/running20201230.png)


### 执行控制台流程
1. 打开流程库
2. 点击控制台流程库，即可获取流程库所有流程包
3. 你可以通过流程包名搜索找到你想要执行的流程包。
4. 选择要执行的版本，点击执行。
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-Console-0.png)


### 终止流程

当流程正在执行时，用户可以随时终止流程运行。

1. 打开本地/控制台流程库，找到正在运行的流程。
2. 在右侧按钮中点击**终止**。
   >**说明：**
   >
   >可以使用快捷键Shift+F5终止当前正在运行的流程。

3. 确认**终止**后，机器人将强制终止正在运行的流程，无论流程运行到哪一步。**终止**操作无法撤回，无法删除。请谨慎操作。

    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-Kill-0.png)


### 查看日志（包括录制的流程执行视频）

当流程执行结束后，用户可查看日志。
1. 打开本地/控制台流程库，找到运行过的流程
2. 点击**日志**打开此流程执行记录的日志文件夹，包括视频文件。
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-Log-0.png)

### 删除流程
支持用户删除本地流程库流程，若删除控制台流程库中的流程需前往控制台。
1. 打开本地流程库，选中将要删除的流程及版本号
2. 点击**删除**弹窗确认是否删除当前版本。点击“确定”则把此版本流程删除。
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/robot-deleteflow-1.png)
