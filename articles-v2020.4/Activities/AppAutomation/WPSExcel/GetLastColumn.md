# 获取末列号

获取工作表或指定行有数据区域的最后一列列号

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **工作表** ：获取末列号操作所属工作表。仅支持字符串变量和字符串
- **行号** ：获取末列号的所属行索引（例：1，即获取第一行的末列号）。当此项为空时，取整表数据区域最后一列列号。仅支持整型变量和整型

### 输出

**末列号** ：将取到的末列号存储在此整型变量内

## 使用示例

1. 新建一个 Excel 文件，在 A1: B8 处填入需要被读取的值:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps29.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **获取末列号** 组件至 **打开/新建** 组件中，并配置工作表名称和行号，输出的列号赋值给变量:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps37.png)

4. 拖入 **获取末行号** 组件至 **打开/新建** 组件中，并配置工作表名称和列号，输出的行号赋值给变量:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps38.png)

5. 拖入 **写入日志** 组件，来显示读取行号和列号的内容:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps39.png)

6. 点击流程运行，观察运行结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps40.png)