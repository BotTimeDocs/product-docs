# 获取文本

## 视频示例

## 概述

获取指定元素的文本。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 目标

- **[选择器](../Appendix/Selector.md)**：用于指示要点击的目标位置。可通过点击**指定元素**自动生成，仅支持字符串变量和字符串。

### 输出

- **文本**：将获取到的文本内容存储到此变量，仅支持字符串变量和字符串。

## 使用示例

1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](./MobileConnect.md)。
2. 在连接设备组件内拖入一个**获取文本**组件。
3. 单击**获取文本**组件中的“指定元素”链接，指定需要获取的元素的文本。

    ![指定获取元素文本](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settinggettext20201223.png)

4. 配置**获取文本**组件的属性参数。

    ![配置获取文本属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingtextproperty20201223.png)

5. 在**获取文本**组件的下方，拖入一个**确认框**组件，并配置属性参数，将获取到的属性文本值输出至确认框中。

    - 标题：输入确认框的标题，如，"确认获取文本的值"
    - 描述：输入确认框中的正文内容，如，"GetText:"+GetText

6. 保存并运行流程，可看到将获取到的文本内容输出至确认框中的运行效果，如下图所示。

    ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/showgettext20201223.png)

