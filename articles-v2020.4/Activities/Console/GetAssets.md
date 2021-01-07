# 获取资产

可实现获取企业版控制台数据中心设置的资产。在编辑器或机器人运行时基于当前激活信息的控制台权限。
仅支持企业版。


## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件
- **超时（毫秒）**：指定此组件的执行时间。单位为毫秒（ms）,1000ms = 1s。包含匹配超时（毫秒）。若超出此时间，组件还未执行，会抛出错误。


### 输入
- **资源组** ：输入或从下拉列表选择资源组。支持字符串变量或字符串
- **资产名称** ：输入或从下拉列表选择资产名称。支持字符串变量或字符串

### 输出

- **值** ：输出资产的值。仅支持变量。注意：变量类型依赖于所获取资产在控制台设置的值类型，例如获取凭证类资产，变量类型应为 Encoo.DataType.Credential；可使用Credential.UserName和Credential.Password获取用户名和密码



1. 拖入**获取资产**组件至项目流程中，并设置变量result(String)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_1.png)

2. 双击打开获取资产，选择资源组和资源名称，在输出中添加变量result,如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_2.png)

3. 点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_3.png)

注：组件需要私有化部署，控制端设置如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_4.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_5.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetAssets_6.png)
