# 打开应用软件
打开手机上指定的应用软件。

## 属性

### 基本

- **后延迟（毫秒）**：在执行组件操作之后的延迟时间（以毫秒为单位）。
- **前延迟（毫秒）**：在开始执行组件操作之前的延迟时间（以毫秒为单位）。
- **失败后继续**：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **显示名称**：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。

### 目标

- **应用软件名**：Bundle Id 的应用名称，系统自动生成，可编辑且可为空，并不做定位效用。
- **应用标识名**：应用软件的 Bundle ID 。

## 操作样例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](/articles-v2020.4/Activities/PhoneAutomation/MobileConnect.md)。
2. 在连接设备组件内拖入一个**打开应用软件**组件。
3. 单击**打开应用软件**组件中的**选择软件**链接，选择需要打开的软件名称并单击“运行”按钮，这里以打开“Metro大都会”软件为例，如下图所示。
   ![选择软件名称](https://docimages.blob.core.chinacloudapi.cn/images/Activities/openapp20201222.png)
4. 在编辑器界面，查看配置完成的流程如下图所示。
   ![配置流程](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingopenapp20201222.png)

5. 保存并运行流程,运行效果如下图所示。
   ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/showopenapp20201222.png)