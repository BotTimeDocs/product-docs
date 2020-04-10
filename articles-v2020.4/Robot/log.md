# 机器人日志

你可以通过右键系统托盘，打开系统日志。

系统日志罗列了流程运行的详细日志，包含时间戳和INFO，ERROR，WARNING级别日志。

日志存储在：[安装路径]\Encoo Robot\Service\log\Executor

日志原则上按天记录，若单天日志超过5MB则会创建同日期的另一个文件。

![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/robotlog.png)

通过控制台下发执行的流程，机器人将会把日志上传至控制台。

上传至控制台的日志只包含ERROR，WARNING级别日志，若产生ERROR日志，机器人将自动在该时间点截图。截图将一并上传到控制台。

发送到控制台的日志在本地仍可以查看到。