# 集合转数组

## 视频示例

## 概述

将集合转换为数组，一般用来遍历集合。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

**集合**：欲被转换为数组的集合，可接变量。

### 输出

**数组**：被转换成的数组对象的结果，仅可接变量。

## 使用示例

1. 拖入一个**集合转数组**组件至流程中。
2. 定义两个流程变量：
   ![定义变量](https://docimages.blob.core.chinacloudapi.cn/images/Activities/varialscollect20201218.png)
    - CL：此变量用于存放需要转换的集合，变量类型定义为`List<Int32>`，并输入默认值为`new List<Int32> {1,3,5,7,9};`
    - array：此变量用于存放转换后的数组的值，变量类型定义为`Int32[]`  
3. 配置**集合转数组**组件的属性。
   ![赋值](https://docimages.blob.core.chinacloudapi.cn/images/Activities/assigncollect20201218.png)

    - 集合：将定义的CL变量赋值给集合，输入`CL`
    - 数组：将定义的array变量赋值给数组，输入`array`  
4. 在**集合转数组**组件的下方拖入一个**写入日志**组件，并双击配置该组件，输入`"集合转数组的值为"+array[0]`，表示获取数组中的第一个值。
5. 保存并运行流程。
6. 在输出窗口查看运行结果。
   ![查看运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/listtoarrayresult20201218.png)