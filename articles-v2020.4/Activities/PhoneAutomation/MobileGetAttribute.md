# 获取元素属性值
输出指定元素的属性值，并将其存储在输出变量属性值中。

## 属性

### 基本
- **后延迟（毫秒）**：在执行组件操作之后的延迟时间（以毫秒为单位）。
- **前延迟（毫秒）**：在开始执行组件操作之前的延迟时间（以毫秒为单位）。
- **失败后继续**：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **显示名称**：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。

### 输入

- **属性名**：要获取目标元素的属性名，仅支持字符串变量和字符串。
  
### 输出
- **属性值**：获取到的属性值内容，仅支持字符串变量和字符串。
  
### 目标
- **[选择器](../Appendix/Selector.md?_v=v2020.4)**：要获取的特定UI元素。可通过点击指定元素自动生成，仅支持字符串变量和字符串。
  

## 操作样例
1. 拖入一个连接设备组件至流程中，具体参见[连接设备组件 - 操作样例](/articles-v2020.4/Activities/PhoneAutomation/MobileConnect.md)。
2. 在连接设备组件内拖入一个**获取元素属性值**组件。
3. 单击**获取元素属性值**组件中的“指定元素”链接，指定需要获取的元素。
   ![指定获取元素](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settinggettext20201223.png)

4. 在**获取元素属性值**组件中的下拉框中，选择需要获取的属性名，如下图所示。
   ![获取元素属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getelementattribute20201223.png)
5. 配置**获取元素属性值**组件的属性参数。
   ![配置获取元素属性](https://docimages.blob.core.chinacloudapi.cn/images/Activities/dimvarial20201223.png)
6. 在**获取元素属性值**组件的下方，拖入一个**写入日志**组件，并配置属性参数，将获取到的元素属性值输出至日志中。
    - 日志级别：下拉选择日志级别，如，Info
    - 日志内容：输入日志内容，如，"获取到的元素属性值为："+GetElementAttribute
7. 保存并运行流程，可看到将获取到的元素属性值输出至日志中的运行效果，如下图所示。
   ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/showgetattribute20201223.png)