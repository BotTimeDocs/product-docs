# 打开项目报错

## 限制条件

1. 通过编辑器导出的流程包，需要使用相同或更高版本的编辑器导入打开已知的流程包
2. 对于私有市场中的组件，需要保证网络连接畅通

## 常见原因

1. 编写流程时使用的编辑器版本是低版本的，而打开流程项目时使用的是高版本编辑器打开的。

    ![原因一](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/00120220506.png)

2. 流程中有组件市场或代码市场中的一些依赖项，如果网络异常/断开，则无法下载这些私有市场里的组件

    ![原因二](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/00220220506.png)

## 常见排查步骤

1. **打开项目时，在流程图编辑区域中出现部分组件”未能生成 XXX 视图“。**

    ![未能生成视图](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/00320220506.png)

    解决办法：

    - Step1：关闭当前编辑器
    - Step2：在文件资源管理器中输入 `%UserProfile%\.nuget\packages\`，将 packages 这个文件夹删除
    - Step3：重新打开编辑器，以重新生成 packages 文件夹

2. **打开项目时，报错”[错误]  Method not found:'System.string Encoo.Automation.CommonActivity.BaseSelectorActivity.get_Storeld()“**

    ![未找到方法](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/00420220506.png)

    解决办法：

    - Step1：复制 ` %UserProfile%\.nuget\packages\automationactivity` 路径至资源管理器中，查看该路径下最高版本是多少

    - Step2：复制 `%UserProfile%\AppData\Local\EncooStudio\{version}\buildinActivities` 路径至资源管理器中，查看该路径下的 `automationactivity` 版本号是多少

    - Step3：如果【Step1】和【Step2】中的版本号不一致，说明本地有高版本的依赖项，此时可以
        - 方法一：升级编辑器和机器人到最新版本（推荐）
        - 方法二：升级到【Step1】的编辑器的版本，需要知道【Step1】里面的 automationactivity 的版本对应的编辑器的版本
    - Step4：关闭编辑器，清空 `%UserProfile%\.nuget\packages`，重新打开编辑器，新建一个项目，关闭这个项目，断网，打开报错的项目