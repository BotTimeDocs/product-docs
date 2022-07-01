# 插入公式

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/InsertFormula.mp4"></video>

## 概述

向单元格插入公式，并填充公式运行后的结果。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **单元格** ：执行插入公式操作的目标单元格，即，接收执行公式的结果，支持区域。
- **工作表** ：插入公式的目标单元格所属工作表。
- **公式** ：插入的公式。

    > **说明**：
    >
    > 支持两种写法，两种写法均可省略等号
    >
    >- 含公式名，如，SUM(A1, A2)
    >- 不含公式名，如，A1+A2。

### 输出

- **执行结果**：将公式执行结果存储在此变量。

## 使用示例

**前置必要组件**：[打开/新建](../TableExcelWPS/OpenExcel.md)

**此流程执行逻辑**：在“Sheet1”工作表的 A2 单元格中插入公式“SUM(A1: D1)”。

![配置插入公式组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InertFormula2.png)

**执行结果**：

![执行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InertFormula3.png)
