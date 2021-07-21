# 调用流程（引用项目）

## 视频示例

## 概述

该组件实现调用已引用的项目的流程文件，供当前项目流程使用。

>**说明：**
>
>在使用该组件前，需在项目面板中，右击项目名称，选择“引用项目”来引用项目的流程文件（一般为 dgs 文件）。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **参数**：点击“设置参数”后在弹窗设置参数，并设置名称、方向、类型及值。在弹窗中点击“导入参数”可直接把被调用文件的参数写入到参数列表。

## 使用示例

1. 在编辑器编辑页面，右击项目名称，在弹出的菜单中选择**引用项目 > 选择文件**。

   ![image-20201207160513550](https://docimages.blob.core.chinacloudapi.cn/images/Activities/image-20201207160513550.png)

2. 在打开文件对话框中，选择需要引用的dgs格式的项目文件。

    > **说明：**
    >
    > - dgs格式的文件是导出项目时生成的项目文件。
    > - 项目文件选择完成后，在当前项目下的**依赖项**中。

    ![image-20201207161108502](https://docimages.blob.core.chinacloudapi.cn/images/Activities/image-20201207161108502.png)

3. 在新建的流程中需要引用流程处，拖入**调用流程（引用项目）** 组件。

![image-20201207161253694](https://docimages.blob.core.chinacloudapi.cn/images/Activities/image-20201207161253694.png)

4. 双击**调用流程（引用项目）** 组件进行配置：选择需调用的流程及流程主文件，如下图所示。

   ![调用流程（引用项目）](https://docimages.blob.core.chinacloudapi.cn/images/Activities/workflowproject20201210.png)

    - 选择项目：下拉选择已引用的项目名称。
    - 选择流程文件：下拉选择已引用的项目流程文件，一般为 xaml 形式的文件。
    - （可选）设置参数：单击“设置参数”按钮，可对当前调用的流程进行设置参数，在弹窗中点击“导入参数”可直接把被调用文件的参数写入到参数列表。

     ![设置参数](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingargument20201217.png)

5. 保存并运行流程。