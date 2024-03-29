# 清除格式

## 视频示例

## 概述

清除 Excel 单元格或区域中的内容格式。

> **说明：**
>
> 该组件需在 Office Excel 的 **打开/新建** 组件内进行使用。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表**：执行“清除格式”操作所属工作表。
- **类型**：选择期望清除的区域的类型。
- **选中区域**：基于选择的“类型”属性，输入需要清除的区域。

### 输出

- **结果**：清除的结果值存储至此变量中。

## 使用示例

**此流程执行逻辑**：将桌面中“研发记录清单.xlsx”文件中的 `"Sheet1"` 工作表中的 `"A1:C2"` 区域中的内容，清除格式。

![配置清除格式](https://docimages.blob.core.chinacloudapi.cn/images/Activities/clearformat20211115.png)
