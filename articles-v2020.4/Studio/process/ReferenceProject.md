# 引用项目

**引用项目** 用于将外部项目引用到当前项目中，作为当前项目的依赖项，在当前项目中通过 **调用流程(引用项目)** 组件实现对该依赖项的调用。

## 操作示例

1. 在编辑器编辑页面，右击项目名称，在弹出的菜单中选择 **引用项目 > 选择文件**。
      ![image-20201207160513550](https://docimages.blob.core.chinacloudapi.cn/images/Activities/image-20201207160513550.png)

2. 在打开文件对话框中，选择需要引用的 dgs 格式的项目文件。

   > **说明：**
   >
   > - dgs 格式的文件是导出项目时生成的项目文件。
   > - 项目文件选择完成后，在当前项目下的 **依赖项** 中。

   ![image-20201207161108502](https://docimages.blob.core.chinacloudapi.cn/images/Activities/image-20201207161108502.png)

3. 在新建的流程中需要引用流程处，拖入 **调用流程（引用项目）** 组件。

   ![image-20201207161253694](https://docimages.blob.core.chinacloudapi.cn/images/Activities/image-20201207161253694.png)

4. 双击 **调用流程（引用项目）** 组件进行配置：选择需调用的流程及流程主文件，如下图所示。
   > **说明：**
   >
   > （可选）单击“设置参数”按钮，可对当前调用的流程进行设置参数。

    ![image-20201207161408189](https://docimages.blob.core.chinacloudapi.cn/images/Activities/image-20201207161408189.png)

5. 保存流程（Ctrl + S）并运行（Ctrl + F5）。
