# 流程库

机器人可以通过桌面点击的方式执行流程，也可以通过控制台集中管理执行流程。

控制台集中管理执行流程详见：[如何下发一个流程](../Console/process/runProcess.md?_v=v2020.4)

本地执行的流程来源分为两种：
1. 本地流程文件文件：通过编辑器导出的流程包（后缀为.dgs的流程压缩包）
2. 控制台流程库:获取机器人所在资源组的[流程包](..\Console\packages\aboutPackages.md?_v=v2020.4)

**控制台流程库**仅供通过控制台激活的机器人使用。

同一机器人同一时间只能执行一个流程，仅在流程执行结束后，方可执行下一个流程。


### 执行本地流程
1. 打开本地流程库
2. 点击导入流程，将编辑器导出的项目文件（*.dgs）导入本地流程库。
3. 选择你想要执行的流程，你可以输入流程名点击搜索进行查询。
4. 点击执行，将会弹窗确认信息
    
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-ExecuteProcessDialog-0.png)
    
    **注意** ：
    - 若当前流程需要传入参数，点击执行后会弹窗提示输入参数，例如下图中的流程需要3个参数（参数sheetName和cell为String类型；count为Int类型）;
    - 若需要在流程执行过程中录制视频，可勾选“录制视频”选项，并选择保留什么状态的视频；
    - 支持选择当前流程以什么权限执行；

5. 点击确认，流程在快速准备后将自动执行。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-0.png)


### 执行控制台流程
1. 打开流程库
2. 点击控制台流程库，即可获取流程库所有流程包
3. 你可以通过流程包名搜索找到你想要执行的流程包。
4. 选择要执行的版本，点击执行。
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-Console-0.png)


### 终止流程

当流程正在执行时，用户可以随时终止流程运行。
1. 打开本地/控制台流程库，找到正在运行的流程
2. 在右侧按钮中点击**终止**
3. 确认**终止**后，机器人将强制杀死正在运行的流程，无论流程运行到哪一步。**终止**操作无法撤回，无法删除。请谨慎操作。
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
