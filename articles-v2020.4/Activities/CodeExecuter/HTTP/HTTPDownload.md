# 下载文件

此组件可以发送下载请求并输出文件

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **URL** ：输入请求的URL；仅支持字符串变量和字符串
- **保存至目录** ：输入文件将被下载到的目录，若为空则默认为Windows的下载目录；仅支持字符串变量和字符串
- **超时(秒)** ：输入请求超时秒数；仅支持整型变量和整型值
- **同名覆盖** ：输入是否覆盖当前路径的同名文件

### 输出

- **文件路径** ：输出下载的文件本机路径；仅支持变量
## 使用示例

1. 拖入**HTTP下载**组件，设置文件路径变量`path`，变量类型为`String`，**输入**URL`"https://dtapp-pub.dingtalk.com/dingtalk-desktop/win_installer/Release/DingTalk_v5.1.41.19.exe"`，**输入**保存至目录`"D:\下载"`，**输入**超时（秒）`300`，**输出**文件路径`path`，如下图所示：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPDownload1.png)
2. 下载文件成功
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPDownload2.png)
3. 拖入**写入日志**组件，打印文件绝对路径，输入**日志内容**`path`，打印结果为`D:\下载\DingTalk_v5.1.41.19.exe`：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPDownload3.png)
