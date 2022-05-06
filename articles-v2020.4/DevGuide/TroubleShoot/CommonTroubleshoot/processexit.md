# 流程闪退/编辑器卡

## 限制条件

1. 安装编辑器的硬件配置推荐：
   - CPU：四核2.4GHz或更快CPU
   - 内存：8GB RAM
   - 硬盘空间：10 HDD/SSD GB 以上空闲磁盘空间
2. 使用最新版本的编辑器

## 常见排查步骤

1. **在使用编辑器的过程中，突然出现报错”引发类型为"System.OutofMemoryException"的异常。“或卡顿、卡死、闪退等问题。**

    ![异常一](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/000120220506.png)

    ![异常二](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/000220220506.png)

    解决办法：

    Step1：在流程执行时，打开任务管理器，看下编辑器进程的内存的使用率是否高。

    - 如果编辑器内存高的话，可以需要编辑器所在计算机进行扩容或者升级编辑器版本
    - 如果其他程序有占用高内存的话，需要关掉其他占内存高的软件。

    Step2：若以上无法解决问题，排查单流程内的组件是否过多，如果过多，建议将单流程按其功能拆分为多个子流程再执行。
