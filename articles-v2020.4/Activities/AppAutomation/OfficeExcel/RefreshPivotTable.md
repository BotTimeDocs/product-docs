# 刷新透视表

## 视频示例

## 概述


此组件可实现刷新指定透视表的数据

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：透视表所属工作表。仅支持字符串变量和字符串
- **透视表名** ：输入透视表名称。仅支持整型变量和整型

## 使用示例

1. 新建一个透视表 "销售统计", 详情见 [新建透视表](./CreatePivotTable.md)

2. 拖拽 **打开/新建** 组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. 双击打开，并点击 **...** 选择本地 Excel 文档：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. 拖拽 **刷新透视表** 组件到 **打开/新建** 组件中，填写工作表名称 "sheet1"，填写透视表名称 "销售统计"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RefreshPivotTable1.png)

5. 修改 excel 中收入列：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RefreshPivotTable2.png)

6. 运行成功后，透视表汇总项已经更新：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/RefreshPivotTable3.png)
