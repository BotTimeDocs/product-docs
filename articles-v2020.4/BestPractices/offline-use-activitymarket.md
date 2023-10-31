# 离线使用组件市场中的组件

## 概述

本文解决的场景为“在只有公司内网或没有网络的情况下，如何使用组件市场中的组件”。

## 操作思路

1. 在一台有网络的计算机中，使用编辑器安装组件市场中的指定组件
2. 将已有安装路径下的 nupkg 文件拷贝至另一台无网络的计算机中
3. 先在无网络的计算机的编辑器中创建本地组件市场并启用，然后再在本地组件市场中安装并使用指定的组件

![操作思路](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/offlineactivity20220125.png)

## 前置条件

- 有一台有网络的计算机并在该计算机上安装了云扩 RPA 编辑器
- 有一台无网络的计算机并在该计算机上安装了云扩 RPA 编辑器

## 操作步骤

1. 在云扩 RPA 编辑器的组件市场中搜索需要安装的组件，如，“office Word 组件”。

    ![搜索组件](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/officeword20220125.png)

2. 单击该组件右上角的“安装”按钮。

    ![安装组件](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/officewordinstall20220125.png)

3. 在组件市场中复制该组件的 packageId 的值。

    ![复制 packageId](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/packageid20220125.png)

4. 在`C:\%UserProfile%\.nuget\packages`中搜索对应的 packageId 的值，如，“Encootech.OfficeWord”

    ![搜索 packageId](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/searchpackageid20220125.png)

5. 打开该文件夹对应版本的文件夹中，找到以.nupkg 为结尾的文件，拷贝至无网络的计算机中，如：`"D:\"`。

    ![.nupkg](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/nupkgfile20220125.png)

6. 在无网络计算机的编辑器中创建本地组件市场并启用。

    ![创建本地组件市场](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/createlocalmarket20220125.png)

7. 在无网络的计算机中找到“本地组件市场”，安装指定的组件。

    ![离线安装组件](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/installlocalactivity20220125.png)
