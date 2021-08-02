# 排序

## 视频示例

## 概述

对某列进行排序，提供&quot; 升序，降序&quot; 两种排序模式。工作表内所有行数据随之改变

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **工作表** ：执行排序的目标工作表。仅支持字符串变量和字符串
- **列号** ：对此列进行排序操作。填入列索引（例：1，即对第一列进行排序）。仅支持整型变量和整型
- **顺序** ：下拉框选择排序模式为升序或降序

## 使用示例

1. 新建一个 Excel 文件，在 A1: B7 处填入需要被读取的值:

    ![1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps9.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:

    ![2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **排序** 组件至 **打开/新建** 组件中，填写工作表和列号，设置排序规则为降序:

    ![3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps24.png)

4. 点击流程运行，观察运行结果:

    ![4](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps25.png)

5. 将流程中 **排序** 组件的排序规则设置排序规则为升序:

    ![5](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps26.png)

6. 再次点击流程运行，观察运行结果:

    ![6](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps9.png)
