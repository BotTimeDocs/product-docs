# 切换控件

## 视频示例

## 概述

当发送快捷键动作完成后，可判断焦点是否发生改变，若焦点改变，则运行成功；若焦点未改变，则运行失败。

支持桌面端，浏览器暂不支持。

## 属性

### 辅助键

- **Alt** ：勾选时，则模拟点击此键
- **Ctrl** ：勾选时，则模拟点击此键
- **Shift** ：勾选时，则模拟点击此键
- **Win** ：勾选时，则模拟点击此键

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **窗口置顶**：选择运行时的桌面窗口是否置顶，部分界面窗口置顶时无法获取到窗口内的内容，这时需要将此属性设置为不置顶。
- **等待焦点改变** ：勾选时，判断焦点是否改变且仅当焦点改变时才运行成功。不勾选时，不会判断焦点是否改变。

### 目标

- **控件元素** ：接收变量作为接收快捷键的目标元素。属性**控件元素**和**选择器**二者互斥，且均可为空
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示接收快捷键的目标位置。可通过点击**指定元素**自动生成。属性**控件元素**和**选择器**二者互斥，且均可为空。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

### 输入

- **键值** ：模拟点击此键。支持多键值，例如"A,Z"需同时按下的场景，填写"AZ"即可

## 使用示例

1. 拖入**切换控件**组件，指定元素，设置对应的属性值，**等待焦点改变**这个选择如果不勾选的话，效果就跟普通的发送快捷键是一样的：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SwitchControl1.png)

2. 验证元素存在性：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SwitchControl2.png)

3. 指定区域是企业微信窗口：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SwitchControl_selectedZone.png)

4. 运行流程并查看结果，企业微信发送Ctrl + N 快捷键会打开一个新的聊天窗口，也就意味着焦点发生了变化，所以组件执行成功：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SwitchControl1.png)
