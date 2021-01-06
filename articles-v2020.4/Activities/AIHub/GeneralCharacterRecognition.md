# 通用文字识别
默认使用当前用户登录权限，识别通用文字信息。
>**说明:**
>
> 若用户未配置相应服务账号，用户只可使用当日免费服务次数。若想继续使用该服务需前往云扩 [AI HUB](https://aihub.encoo.com/serviceAccount) 配置使用配额。


## 属性
### 基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称。
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误。
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件。
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件。
### 输入
- **参数**：点击组件【设置参数】按钮，可配置如下参数：
  - 服务：可识别的通用文字的种类，目前支持手写数字、手写文本、通用文字(即，普通电子文本。如，网页文本)。
  - 平台：第三方 AI 平台，目前支持百度 AI 、讯飞 AI 、华为云。
  - 图片文件：指定欲识别的图片路径，可接变量，建议使用常用的 jpg、jpeg 和 png 图片格式。
### 输出
- **识别结果**：输出识别后的原始数据（JSON），仅支持变量。


## 操作样例

1. 拖入**通用文字识别**组件至项目流程中，并设置变量result(String)：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GeneralCharacterRecognition_1.png)

2. 双击通用文字识别，选取图片，例："D:\\测试图片.jpg"，输入图片路径，选择需要的类型和对应平台，在输出中添加变量result,如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GeneralCharacterRecognition_2.png)

3. 点击运行，查看运行结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GeneralCharacterRecognition_3.png)