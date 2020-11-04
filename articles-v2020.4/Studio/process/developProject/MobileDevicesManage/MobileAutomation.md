# **手机自动化**

与PC端界面自动化一样，云扩RPA针对手机自动化也提供了一些手机自动化控件，这些控件可以获取到手机上的元素。

## 操作示例

以关闭手机移动数据开关为例，进行介绍。

1. 拖动一个”连接设备“组件至流程中。

![连接设备](https://docimages.blob.core.chinacloudapi.cn/images/Studio/connectdevices20201104.png)

2. 在”移动设备管理器“面板中，单击”复制设备信息“选项。

![复制设备信息](https://docimages.blob.core.chinacloudapi.cn/images/Studio/copydevices20201104.png)

3. 双击流程界面中的”连接设备“组件，单击”一键填充“，自动填充连接设备的信息。

![连接设备](https://docimages.blob.core.chinacloudapi.cn/images/Studio/connectdevicesfullin20201104.png)

4. 在”移动设备管理器“面板中，单击”智能录制器“中的”录制“按钮进行录制。

![智能录制](https://docimages.blob.core.chinacloudapi.cn/images/Studio/recoder20201104.png)

> **说明：**
>
> 智能录制器的操作，请参见”[**智能录制**](developProject/Recording/Recording.md?_v=v2020.4)“。

5. 录制完成的流程，单击”保存“按钮后，自动形成一个序列至“**连接设备**”组件中。

![流程录制完成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/flowdone20201104.png)

6. 单击**运行面板中**的“运行”按钮，运行流程。

![运行](https://docimages.blob.core.chinacloudapi.cn/images/Studio/run20201104.png)

 运行中的流程会单独弹出一个手机界面效果。

![运行过程界面](https://docimages.blob.core.chinacloudapi.cn/images/Studio/runprocessUI20201104.png)