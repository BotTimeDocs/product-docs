# 如何将流程发布成组件

## 概述

本文解决的场景为“将一个流程作为组件的形式供另外一个流程使用”。

## 操作思路

1. 将一个已创建并开发完成的“组件项目”发布至本地或特定私有网络下的组件市场中。
2. 在另一个流程项目或组件项目中，从组件市场中选择本地或私有网络下的组件进行安装和使用。

![操作思路](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/activitymarket20220126.png)

## 前置条件

- 已创建一个组件项目，具体可参见 [创建组件项目](./../Studio/process/CreateProject/CreateLibrary.md)。
- 已创建并启用本地或特定私有网络的组件市场。

## 操作步骤

### 发布组件项目

如果你需要将已创建的组件项目做为可重用的组件，添加到其他自动化项目中，就需要将其打包，发布到组件市场中。

1. 打开创建的组件项目。
2. 在菜单栏，点击“发布到组件市场”。

   ![发布到组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/publishactivities20201112.png)

3. 在弹出的发布窗口中，选择需要发布的目标市场。

    > **说明：**
    >
    > 若选择不到市场，可到“开始 > 设置 > [管理市场](../Studio/market/Market.md)”中创建并启用。

    ![发布组件市场弹窗](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/activitymarket20220127.png)

4. 点击“发布”，完成组件市场的发布。

> 发布同名的组件会算作一个组件的不同版本，需注意修改名称。

## 安装并使用组件

如果你要在另外一个自动化项目中使用该组件包，需要先安装，将其添加为自动化项目的依赖项。

1. 创建一个流程项目，可参见 [创建流程项目](./../Studio/process/CreateProject/CreateProject.md)。
2. 在“市场面板”中，点击“组件市场”，选择已创建的本地或私有网络的组件市场。

    ![本地组件市场](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/localactivitymarket20220127.png)

3. 单击“本地组件市场”中指定组件的“安装”。

    ![组件安装](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/installactivity20220127.png)

4. 已安装完成的组件在该流程项目的“组件面板”中显示。

    ![组件包](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/newactivityproject20220127.png)

5. 在“流程编辑区域”中可以和使用其它组件一样，使用已安装的组件了。
