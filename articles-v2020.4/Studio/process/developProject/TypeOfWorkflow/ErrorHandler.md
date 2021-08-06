# 异常处理流程

## 概述

当流程在运行过程中出现错误时，异常处理流程帮助捕获错误信息并进行处理。

> **说明：**
>
>- 仅当 **流程项目** 中支持“异常处理流程”功能，**组件项目** 中暂不支持。
>- 仅当运行/调试整个流程时，才会调用“异常处理流程”。
>- 同一流程项目中，有且仅有一个该流程。

## 使用示例

1. 在编辑器中设计 **主流程** 和 **异常处理流程**。

    - **主流程（Main.xaml）**：打开云扩官网后弹出一个确认框，再点击官网上的 Logo 图标。

    ![主流程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/cleanup_main20210805.png)

    - **异常处理流程(ErrorHandler.xaml)**：以确认框的形式，展示主流程在运行过程中出现的错误信息。

    ![异常处理流程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/errorhandler20210806.png)

2. 保存并运行流程。
3. 查看流程运行结果：在最终的确认框中显示错误信息。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/runresult20210806.png)
