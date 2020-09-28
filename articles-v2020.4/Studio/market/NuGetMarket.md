# 代码市场 
你可以使用代码市场，获取 NuGet 应用，并将其加入到你编写的 RPA 流程中。

## 获取与使用

![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-0.png)

1. 打开项目
2. 打开代码市场窗口
3. 搜索找到需要安装的代码包
4. 选中并下载

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-1.png)

5. 安装代码包

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-2.png)

6. 安装时，可能需要接受许可证。

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-3.png)

7. 在项目的“依赖项”中可查看下载的代码包信息

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-4.PNG)

    >注意：
    >
    >在每个项目中，只有至少存在一个引用时，才会设置依赖项。
    >
    >已安装的依赖项仅适用于当前的项目，并且在project.json文件中可以看到每个项目的依赖项列表。

8. 编辑区域的*导入*中可以搜索到下载的代码包，搜索后点击即可引用到项目中。

    ![代码市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-5.PNG)


## 已安装代码包

在代码市场窗口中，还存在一个其他分类：已安装代码包

* **已安装代码包**仅针对当前项目存在，仅显示当前项目已安装的代码包，通过该页面可以管理项目中的依赖项。

    ![已安装代码包](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/CM-6.PNG)

## 管理依赖项

在代码市场中，可查看依赖项的版本，同时可对依赖项进行添加、更新和删除。
要管理依赖项，点击“市场”->“代码市场”，将打开“代码市场”窗口。

1. 对于未添加依赖项的项目，只需通过搜索相应的代码包，找到并安装它们，即可将所需代码包添加到项目中。 
2. 对于已添加依赖项的项目，通过已安装代码包页面，点击删除即可删除该依赖项，要想更新代码包，只需点击更新按钮。