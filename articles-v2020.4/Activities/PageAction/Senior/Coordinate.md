# 坐标点击

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/CoordinateClick.mp4"></video>

## 概述

根据绝对坐标点击指定的用户界面元素。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 点击

- **点击类型** ：下拉选择模拟鼠标点击的类型。
- **横/纵坐标** ：在Windows操作系统上，屏幕上的每一点都有一个唯一的坐标，坐标由两个整数组成：一个称为x（即，横坐标）,另一个称为y（即，纵坐标）。
- **鼠标键** ：选择模拟鼠标点击操作的鼠标键（左键、右键和中键。

### 可选项

- **辅助键** ：用于添加辅助键，实现在点击时同时按下辅助键的效果。

## 使用示例

- **前置必要组件**：[获取鼠标位置](../../MouseKeyboard/GetMousePosition.md)

- **此流程执行逻辑**：在获取到的鼠标位置处点击，查看界面元素。

    ![配置坐标点击组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Coordinate-2.png)
