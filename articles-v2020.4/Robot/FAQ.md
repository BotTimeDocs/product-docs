# 常见问题

1. **Q：重装计算机系统后，机器人的机器码会发生变化吗？**

    **A:** 会发生变化。机器人的机器码在不同Windows用户下是不同的，而重装了系统后，用户信息就没有了，所以机器码也会发生变化。

2. **Q：机器人的默认安装目录是什么？**

   **A：** `%programfiles(x86)%\Encoo Robot`

3. **Q：机器人的系统日志的默认路径是什么？**

   **A：** `%programfiles(x86)%\Encoo Robot\Logs`。

4. **Q：机器人的安装日志的默认路径是什么？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Installation`。

5. **Q：如何撰写Cron 表达式，使流程每天7:00-8:00，每20分钟执行一次 ？**

   **A：** `0 0/20 7,8 * * ?`，可参见[在线Cron表达式生成器](https://www.bejson.com/othertools/cron/)。

6. **Q：什么是Cron表达式，怎么使用？**

   **A：** 具体可参见[Cron表达式详解](https://www.cnblogs.com/yanghj010/p/10875151.html?wework_cfm_code=MEUlenv2IN4vo7D10vYW9eLlYMwLm8xSqDjffgjTGvQ9iGFipvqTLczAoPP5NOEVCs1L7n3RwewZnUC0CAW8z5BR%2F0XT3rI9tRzw6tr0hUp3XrxcSQT3cCY%3D)。