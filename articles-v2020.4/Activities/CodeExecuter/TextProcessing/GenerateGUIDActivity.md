# 生成GUID

获取一个新的GUID。

>**说明:**
>
>全局唯一标识符（GUID，Globally Unique Identifier）是一种由算法生成的二进制长度为128位的数字标识符。在 Windows 平台上，GUID 广泛应用于微软的产品中，用于标识如注册表项、类及接口标识、数据库、系统目录等对象。


## 属性
### 基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件。
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件。

### 输出
- **GUID** ：输出生成的GUID的值存储于该变量中，仅支持字符串变量。
## 操作样例
1. 拖入**生成GUID**组件至项目流程中
![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GenerateGUIDActivity2021010501.png)

2. 拖入其它组件至流程中，例：**写入日志**组件，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GenerateGUIDActivity2021010502.png)

3. 点击运行，成功生成GUID，如下图：

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GenerateGUIDActivity2021010503.png)