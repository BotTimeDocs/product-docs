# 复制粘贴区域

## 视频示例

## 概述

实现将指定工作表中的区域数据，复制并粘贴到目标工作表区域。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **目标工作表**：欲被粘贴至的目标工作表。
- **目标区域**：欲被粘贴至的目标工作表区域。
- **源工作表**：欲被复制的源工作表。
- **源区域**：欲被复制的源工作表中的区域。

## 使用示例

1. 准备一份 Excel 工作表数据，计划将 Sheet1 中的 B 列数据复制粘贴至 Sheet2 中的 A 列。   

   ![数据准备](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sheet1andsheet220201217.png)

2. 拖入一个 Office Excel 的 **打开/新建** 组件至流程中。
3. 配置 **打开/新建** 组件的属性参数。

    - 文件路径：输入需要打开进行复制粘贴数据操作的文件路径，如，"C:\Users\wangxin\Desktop\A.xlsx"

4. 双击该组件，拖入一个 **复制粘贴区域** 组件至 **打开/新建** 组件中。
5. 配置 **复制粘贴区域** 组件的属性参数，如下图所示。

   ![属性配置](https://docimages.blob.core.chinacloudapi.cn/images/Activities/copyandpaste20201217.png)  

    - 源工作表：输入需要复制数据的工作表名称，如，"Sheet1"
    - 源区域：输入需要复制数据的工作表中的数据区域，如，"B2: B11"
    - 目标工作表：输入需要粘贴数据的工作表名称，如，"Sheet2"
    - 目标区域：输入需要粘贴数据的工作表中的数据区域，如，"A2: A11"

6. 保存并运行流程。
7. 在目标工作表 Sheet2 中查看粘贴后的数据。

   ![结果数据](https://docimages.blob.core.chinacloudapi.cn/images/Activities/copyandpasteresult20201217.png)
