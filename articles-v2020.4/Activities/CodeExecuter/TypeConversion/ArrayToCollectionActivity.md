# 数组转集合

## 视频示例

## 概述

将数组转换为集合，一般用来遍历数组。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 输入

- **数组**：欲被转换为集合的数组，可接变量。

### 输出

- **集合**：被转换成的集合对象的结果，仅可接变量。

## 使用示例

1. 拖入一个**数组转集合**组件至流程中。
2. 定义两个流程变量：
   ![定义变量](https://docimages.blob.core.chinacloudapi.cn/images/Activities/varials20201218.png)
    - CL：此变量用于存放转换后的集合的值，变量类型定义为`List<Int32>`
    - array：此变量用于存放待转成集合的数组，变量类型定义为`Int32[]`，并输入默认值为`new int[]{1,3,5,7,9};`  
3. 配置**数组转集合**组件的属性。
   ![赋值](https://docimages.blob.core.chinacloudapi.cn/images/Activities/assign20201218.png)

    - 集合：将定义的CL变量赋值给集合，输入`CL`
    - 数组：将定义的array变量赋值给数组，输入`array` 
 
4. 在**数组转集合**组件的下方拖入一个**写入日志**组件，并双击配置该组件，输入`"数组转集合的值为"+CL.First()`，表示获取集合中的第一个值。
5. 保存并运行流程。
6. 在输出窗口查看运行结果。
   ![查看运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/arraytolistresult20201218.png)