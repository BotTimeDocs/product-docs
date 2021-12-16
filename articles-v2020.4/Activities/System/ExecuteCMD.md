# 执行命令行

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ExcuteCMD.mp4"></video>

## 概述

执行 CMD 命令行，并提供返回值。如，使用命令行实现 60 秒后定时关机： “shutdown -s -t 60”。

> **说明：**
>
> 此组件也支持对 Python 文件的操作，例如：在“命令行”属性中填写“Python Test.py arg1 arg2”, 其中“arg1”和“arg2”为参数。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作目录** ：指定运行命令的工作目录
- **命令行** ：执行该命令行。仅支持字符串变量和字符串

### 输出

- **输出**：将命令行执行后的结果存储到此变量

## 使用示例

**此流程执行逻辑**：执行 cmd 命令，并将执行结果保存至“result”变量中。

![配置执行命令行组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executeCmd-2.png)

## 常见问题

1. **Q：执行"cmd /c query session"命令失败，报错：“`query`不是内部或外部命令，也不是可运行的程序或批处理文件”**

    **A：**

    **【原因排查与分析】**

    64位的计算机上，有“c:\Windows\System32”和“c:\Windows\SysWOW64”两个目录，这两个目录下都有cmd.exe。

    如果应用程序是32位，则默认会调用SystemWOW64下面的cmd.exe（即，c:\Windows\SysWOW64\cmd.exe），因为编辑器的Executor的编译选项是Any CPU且勾了首选32位平台。

    **【短期解决办法】**

    step1：把System32下面的query.exe复制到SystemWow64下。
    step2：在命令中使用如下方式，强制使用System32下的cmd.exe，即，`@"c:\windows\SysNative\cmd.exe /c query session"`
