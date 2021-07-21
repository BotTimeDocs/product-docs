# 获取结构化数据

## 视频示例

## 概述

获取手机端指定页面的结构化数据，目前仅支持桌面应用。

>**说明：**
>
> Android仅能获取可视区域内的数据，需要手动滑动获取更多数据。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **XML数据**：定义从网页中提取哪些数据。
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：用于指示要获取数据的目标区域。可通过点击**指定数据源**自动生成。仅支持字符串变量和字符串。

### 输出

- **数据表**：将获取到的结构化数据存储到此变量。

## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**获取结构化数据**组件。
3. 单击**获取结构化数据**组件中的“指定元素”链接，指定需要获取的结构化数据。

    ![指定获取结构化数据](https://docimages.blob.core.chinacloudapi.cn/images/Activities/mobilegetstructdata20210317.png)

4. 在弹出的获取结构化数据对话框中，按照向导进行获取元素。

   >**说明：**
   >
   > - 如果没获取到结构化数据，提示“请指定数据源内第二个元素”，单击“下一步”进行指定元素。
   > - 如果已获取到结构化数据，将弹出“获取结构化数据”属性界面，用于配置获取结构化数据的列名称及配置属性以获取更多数据。

5. 获取结构化数据完成后，可预览数据，如下图所示。

    ![预览结构化数据](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getstructdatapreview20210317.png) 

6. 配置**获取结构化数据**组件的属性参数。

    ![配置获取结构化数据属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getstructdataproperty20210317.png)

7. 在**获取结构化数据**组件的下方，拖入一个**预览数据表**组件，并配置属性参数，将获取到的数据输出至数据表中。

    - 数据表：填写已输出的数据表对应的变量，如，`DT`。

8. 保存并运行流程，可看到运行效果，如下图所示。

    ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getstructdataresult20210317.png)
