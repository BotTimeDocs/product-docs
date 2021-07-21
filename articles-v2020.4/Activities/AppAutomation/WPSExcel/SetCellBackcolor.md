# 设置单元格背景色

## 视频示例

## 概述

对指定单元格进行填充背景色操作。提供拾色器辅助色号的填写，同时可填入&quot; 获取单元格背景色&quot; 的输出变量作为指定单元格的背景色

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **单元格** ：填充颜色的目标单元格，可填入单元格地址或单元格区域。此处不可为空，否则运行失败
- **工作表** ：目标单元格所属工作表。仅支持字符串变量和字符串
- **颜色** ：取此值作为填充色。可手动输入或使用拾色器辅助

## 使用示例

1. 新建一个 Excel 文件:
    ![1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps20.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
    ![2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **设置单元格背景色** 组件，填写工作表和单元格位置以及需要设置的颜色代码:
    - 举例：红色为#FF0000
    ![3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps21.png)

4. 点击流程运行，观察运行结果:
    ![4-1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps22.png)
    ![4-2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps23.png)
