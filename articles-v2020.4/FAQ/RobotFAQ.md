# 机器人 FAQ

## 安装相关

1. **Q：机器人的默认安装目录是什么？**

    **A：** `%programfiles(x86)%\Encoo Robot`

2. **Q：机器人的系统日志的默认路径是什么？**

    **A：** `%programfiles(x86)%\Encoo Robot\Logs`。

3. **Q：机器人的安装日志的默认路径是什么？**

    **A：** `%UserProfile%\AppData\Local\Encoo\Installation`。

## 流程库相关

1. **Q：机器人中只能导入流程项目dgs,那如何运行组件项目egs?**

    **A：** 组件项目不能运行的，组件项目相当于一个组件包，需要用流程项目在组件市场去安装这个组件项目，然后把这个组件拖入到流程里面去使用。

## 定时任务相关

1. **Q：什么是Cron表达式，怎么使用？**

    **A：** 具体可参见[Cron表达式详解](https://www.cnblogs.com/yanghj010/p/10875151.html?wework_cfm_code=MEUlenv2IN4vo7D10vYW9eLlYMwLm8xSqDjffgjTGvQ9iGFipvqTLczAoPP5NOEVCs1L7n3RwewZnUC0CAW8z5BR%2F0XT3rI9tRzw6tr0hUp3XrxcSQT3cCY%3D)。

2. **Q：如何撰写Cron 表达式，使流程每天7:00-8:00，每20分钟执行一次 ？**

    **A：** `0 0/20 7,8 * * ?`，可参见[在线Cron表达式生成器](https://www.bejson.com/othertools/cron/)。

3. **Q：云扩机器人是否支持同时执行多个任务？**

    **A：** 任务只能一个一个地运行，处理完一个任务才能处理其它任务。

## 其他

1. **Q：重装计算机系统后，机器人的机器码会发生变化吗？**

    **A:** 会发生变化。机器人的机器码在不同Windows用户下是不同的，而重装了系统后，用户信息就没有了，所以机器码也会发生变化。

2. **Q：执行机器人一定要安装编辑器吗？执行报错但不知道如何解决?**

   ![执行机器人](https://docimages.blob.core.chinacloudapi.cn/images/Robot/executerobot20210825.png)

    **A：** 可以不安装编辑器，尝试重启“Encoo Robot Service”服务。

   ![机器人服务](https://docimages.blob.core.chinacloudapi.cn/images/Robot/robotservice20210825.png)
