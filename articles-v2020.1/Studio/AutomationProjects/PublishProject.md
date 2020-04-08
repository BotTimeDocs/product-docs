# 发布自动化项目
**发布自动化项目**允许你将编辑成功的自动化流程发布到控制台或流程市场中，以便后续机器人执行或共享流程。

自动化项目发布到控制台后，将存储在流程包管理页面，以便分配给指定机器人执行。而发布到流程市场后，将存储在你指定的流程市场中，以便实现共享。

要实现发布流程，从工具栏->发布中选择你想要发布的位置，然后点击它。

<!-- ![发布项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/choosePosition.PNG) -->

## 发布流程
1. 创建一个自动化项目。项目示例参看[创建自动化项目](./CreateProject.md)
2. 在工具栏->发布选择发布的位置：
    * 发布到控制台
    
        <!-- ![发布到控制台](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/publishToConsole.PNG) -->

        a. 流程包名称默认情况下为项目名称，可进行更改。</br>
        b. 将最新版本号添加至项目中。若更改版本号信息，需注意的是最新版本号要大于当前版本号。</br>
        c. (可选)备注主要用于对当前发布的流程进行简单介绍。

    * 发布到流程市场
    
        <!-- ![发布到流程市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/publishToFlowmarket.PNG) -->

        a. 选择流程市场，以作为自动化项目最终的存储位置。首次发布需通过“管理流程市场”配置你的市场，具体步骤请参考[管理流程市场](../Market.md)。</br>
        b. 流程包名称默认情况下为项目名称，可进行更改。</br>
        c. 将最新版本号添加至项目中。若更改版本号信息，需注意的是最新版本号要大于当前版本号。</br>
        d. (可选)图标主要用于对当前发布的流程进行标识。</br>
        e. 输入描述信息，以介绍此流程具体的作用。</br>
        f. (可选)标签用于定义当前流程。

3. 点击“发布”，该项目将会发布到指定位置。
4. 发布成功后，将显示一个信息提示框，显示：
    * 发布成功的项目名称
    * 该项目的版本号

        <!-- ![发布成功](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/publishSuccess.PNG) -->