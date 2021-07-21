# 键盘触发器

## 视频示例

## 概述

监听系统范围键盘事件后，触发指定操作。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **触发器等待时间**：等待触发时间。
- **辅助键**：含有： 无，Shift, Ctrl, Alt, Win。 实现在同时按下辅助键的效果。

### 输入

- **键值**：键盘按下的指定的键值。

## 使用示例

1. 拖入一个“键盘触发器”组件至流程中。
2. 双击打开“键盘触发器”组件。
3. 设置“键盘触发器”组件属性。

    ![键盘触发器](https://docimages.blob.core.chinacloudapi.cn/images/Activities/keyboardtrigger20210508.png)

    - 触发等待时间：等待触发的时间，如，`00:00:10`。
    - 键值：键盘按下的键值，如，`"4"`。

4. 在该组件的“触发后操作”区域中，拖入一个“提示框”组件。
5. 设置“提示框”组件的属性。

    ![提示信息](https://docimages.blob.core.chinacloudapi.cn/images/Activities/info20210508.png)

    - 提示信息：输入提示的文字内容，如，`"键盘触发成功"`。
    - 提示时长（秒）：输入提示框展示时长，如，`500`。

6. 保存并运行流程。
7. 按下键盘数字键“4”。
8. 在桌面右下角，查看运行效果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/keyboardresult20210508.png)
