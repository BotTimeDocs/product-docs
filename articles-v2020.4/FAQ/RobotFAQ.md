# 机器人 FAQ

## 安装相关

1. **Q：机器人的默认安装目录是什么？**

    <details>

    <summary> 点击展开 </summary>

    **A：** `%programfiles(x86)%\Encoo Robot`

    </details>

2. **Q：机器人的系统日志的默认路径是什么？**

    <details>

    <summary> 点击展开 </summary>

    **A：** `%programfiles(x86)%\Encoo Robot\Logs`。

    </details>

3. **Q：机器人的安装日志的默认路径是什么？**

    <details>

    <summary> 点击展开 </summary>

    **A：** `%UserProfile%\AppData\Local\Encoo\Installation`。

    </details>

4. **Q：机器人的流程执行的任务记录的日志默认路径是什么？**

    <details>

    <summary> 点击展开 </summary>

     **A：** `%UserProfile%\AppData\Local\Encoo\Encoo Robot\JobLogs`。

    </details>

## 升级相关

1. **Q：机器人登录界面报错“未知异常”，如何处理？**

    <details>

    <summary> 点击展开 </summary>

     **A：** 一般情况下是机器人版本与控制台版本不匹配导致，如果是 V3 控制台的私有化用户，需要联系对应的实施退回与之匹配的机器人版本。

    </details>

## 流程库相关

1. **Q：机器人中只能导入流程项目 dgs, 那如何运行组件项目 egs?**

    <details>

    <summary> 点击展开 </summary>

    **A：** 组件项目不能运行的，组件项目相当于一个组件包，需要用流程项目在组件市场去安装这个组件项目，然后把这个组件拖入到流程里面去使用。

    </details>

2. **Q：不同账号登录如何看到不同的流程库信息？**

    <details>

    <summary> 点击展开 </summary>

    **A：** 可在控制台的“RPA 中心 > 流程包管理”中查看。

    </details>

## 定时任务相关

1. **Q：什么是 Cron 表达式，怎么使用？**

    <details>

    <summary> 点击展开 </summary>

    **A：** 具体可参见 [Cron 表达式详解](https://www.cnblogs.com/yanghj010/p/10875151.html?wework_cfm_code=MEUlenv2IN4vo7D10vYW9eLlYMwLm8xSqDjffgjTGvQ9iGFipvqTLczAoPP5NOEVCs1L7n3RwewZnUC0CAW8z5BR%2F0XT3rI9tRzw6tr0hUp3XrxcSQT3cCY%3D)。

    </details>

2. **Q：如何撰写 Cron 表达式，使流程每天 7: 00-8: 00，每 20 分钟执行一次 ？**

    <details>

    <summary> 点击展开 </summary>

    **A：** `0 0/20 7,8 * * ?`，可参见 [在线 Cron 表达式生成器](https://www.bejson.com/othertools/cron/)。

    </details>

3. **Q：云扩机器人是否支持同时执行多个任务？**

    <details>

    <summary> 点击展开 </summary>

    **A：** 任务只能一个一个地运行，处理完一个任务才能处理其它任务。

    </details>

## 流程执行相关

1. **Q：日志提示，类似“流程执行失败：流程尚未开始执行-Windows 用户 [RPA-WIN2012DOM\Administrator] 当前未登录”的错误，如何解决？**

    <details>

    <summary> 点击展开 </summary>

    **A:** 勾选机器人“设置”中的“RDP 远程”选项，详情参见 [RDP 远程](../Robot/Settings/Basic.md)。

    </details>

2. **Q：为什么加入域的电脑，RDP 会话保持失败，在日志文件中没有 RdpSessionMaster 开头的 log 文件？**

    <details>

    <summary> 点击展开 </summary>

    **A:** 在当前电脑的“Windows 设置 > 更新和安全”中，保证“Windows 更新”补丁为最新。

    </details>

3. **Q：日志提示“拒绝访问和错误代码 7045”的错误，如何解决？**

    <details>

    <summary> 点击展开 </summary>

    **A：** 在当前电脑的“Windows 设置 > 远程桌面”中，将当前用户添加至远程用户中。

    ![添加远程用户](https://docimages.blob.core.chinacloudapi.cn/images/Robot/7045.png)

    </details>

## 其他

1. **Q：重装计算机系统后，机器人的机器码会发生变化吗？**

    <details>

    <summary> 点击展开 </summary>

    **A:** 会发生变化。机器人的机器码在不同 Windows 用户下是不同的，而重装了系统后，用户信息就没有了，所以机器码也会发生变化。

    </details>

2. **Q：执行机器人一定要安装编辑器吗？执行报错但不知道如何解决?**

    <details>

    <summary> 点击展开 </summary>

    ![执行机器人](https://docimages.blob.core.chinacloudapi.cn/images/Robot/executerobot20210825.png)

    **A：** 可以不安装编辑器，尝试重启“Encoo Robot Service”服务。

    ![机器人服务](https://docimages.blob.core.chinacloudapi.cn/images/Robot/robotservice20210825.png)

    </details>
