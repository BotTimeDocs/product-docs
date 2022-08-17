# FAQ6：私有化部署

#### Q：如何清理私有化部署中的日志文件？

<font color=5a6877> 【解决方法A7_00001】:如果控制台的系统设置中没有流程日志清理功能，可升级至最新版控制台。如暂时无法升级，但日志文件过大，可手动执行以下脚本处理：

```
cd  {控制台安装目录} #例如在/usr/console/consolev4pvt-4.1.118351
rm -rf data/minio/.minio.sys/multipart/*
rm -rf data/minio/.minio.sys/tmp/*
rm -rf data/minio/v2-robot*
```
控制台目录结构

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/15-1.png"/>


 </font><br><br>
 ---
 <br>

#### Q：控制台存放日志和机器人上传的视频的目录在服务器什么位置？

 <br>

<font color=5a6877> 【解决方法A7_00002】:

这个要看是什么环境， 什么版本的机器人，windows，是放在数据库的`executionDb.rpa_runinstancelogentries`

 </font><br><br>
 ---
 <br>