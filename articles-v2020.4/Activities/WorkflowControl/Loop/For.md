# 循环操作

## 视频示例

## 概述

根据指定的循环次数进行循环操作，类似于 FOR 循环。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **循环次数**：需要使循环体循环的次数，可接变量。

### 输出

- **当前索引**：当前循环的索引值，即，第几次循环，仅可接变量。

## 使用示例

1. 拖入一个“循环操作”组件至流程中。
2. 配置“循环操作”组件的属性。

    - 循环次数：需要使循环体进行执行的次数，如，`2`。
    - 当前索引：每一个循环操作的索引值，创建一个变量 A，如，`A`。

3. 在循环体中，拖入一个“点击”组件，并指定元素为 [云扩官网](https://www.encoo.com/) 的 logo 图标。

    ![指定元素](https://docimages.blob.core.chinacloudapi.cn/images/Activities/forclick20210622.png)

4. 在循环体的“点击”组件下方，拖入一个“写入日志”组件，并配置日志内容为 `"第"+A+"次循环"`。

    ![循环操作流程图](https://docimages.blob.core.chinacloudapi.cn/images/Activities/for20210622.png)

5. 保存并运行流程。
6. 在输出窗口中，查看流程运行结果。

    ![流程运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/forrunresult20210622.png)
