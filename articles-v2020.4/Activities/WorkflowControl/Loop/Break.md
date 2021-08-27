# 终止循环

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/EndTheLoop.mp4"></video>

## 概述

跳出当前整个循环，执行循环后的组件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

## 使用示例

**前置必要组件**：[循环操作（While）](../Loop/While.md)

**此流程执行逻辑**：在 While 循环中，拖入 **流程决策** 组件，设置流程决策的判断条件 `System.DateTime.Now.CompareTo(Convert.ToDateTime(t1)) < 0`，如果值为真（即当前时间早于指定时间），则用 **终止循环** 组件来结束循环，如果值为假，用 **赋值** 组件递增循环变量 count。

![设置终止循环组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/break-2.png)
