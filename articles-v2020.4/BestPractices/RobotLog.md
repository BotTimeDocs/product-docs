# 如何查看机器人的日志

## 应用场景

在日常维护中，日志可以帮助我们快速定位问题的根源，追踪程序执行的过程，追踪数据的变化，以及协助我们进行数据统计、性能分析，还能采集运行环境数据。一般在机器人执行流程时，一旦发生异常，第一件事就是要弄清楚当时发生了什么。机器人当时做了什么操作，环境有无影响，数据有什么变化，是不是反复发生等，然后再进一步的确定大致是哪个方面的问题。确定是机器人的问题之后再交由开发人员去重现、研究、提出解决方案。这时，日志就给我们提供了第一手的资料。那么我们想要的日志到底在哪里。

## 在本地查看日志

在执行流程所在的机器人中，可通过单击“**流程库**”列表中的“日志”或单击“**任务记录**”列表中的“日志”，可查看流程的执行日志信息。

![查看日志](https://docimages.blob.core.chinacloudapi.cn/images/Robot/viewlocallog20211026.png)

本地机器人客户端日志，保存在 `%UserProfile%\AppData\Local\Encoo\Encoo Robot\JobLogs\local` 目录下，里面保存了我们的机器人每一天的执行日志。

![本地日志](https://docimages.blob.core.chinacloudapi.cn/images/Robot/locallog20211026.png)

## 在控制台查看日志

在实际 RPA 应用中，很多场景涉及到的是定时任务以及服务型任务，很多时候我们无法直接访问机器人所在的设备，也就无法直接查看机器人本地的日志了。遇到这种情况呢，不要慌，我们还可以通过控制台，直接查看相应机器人运行流程任务记录的日志。通过登录控制台，在“**RPA 管理 > 任务记录 > 操作 > 查看详情**”中，单击“**查看日志**”，就可以看到我们想要的日志了。

![查看控制台日志](https://docimages.blob.core.chinacloudapi.cn/images/Robot/viewconsolelog20211026.png)

在该页面，可按任务记录的执行次序，查看具体的视频日志及文字日志。

![控制台日志详情](https://docimages.blob.core.chinacloudapi.cn/images/Robot/consoledetail20211026.png)
