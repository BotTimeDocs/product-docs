# 验证文本有效性

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/VerifyTextValidity.mp4"></video>

## 概述

使用正则表达式对整段源文本内容验证是否匹配期望值。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **源文本** ：欲被验证的源文本数据。
- **提取规则** ：点击“设置验证规则”后在弹窗中指定验证的规则。

### 输出

- **验证结果**：验证的结果。

## 使用示例

**此流程执行逻辑**：验证`test@test.com`邮箱是否符合邮箱命名规则，结果保存至`isEmail`变量中。

![配置验证文本有效性组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010402.png)

![配置验证文本有效性组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/VerifyTextActivity2021010403.png)
