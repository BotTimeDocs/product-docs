# 获取 Windows 凭据

获取本机 Windows 凭据管理器中 Windows 凭据分类中的普通凭据。

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **凭据名** ：取此凭据名查找用户名和密码，并将结果保存到输出变量。仅支持字符串变量和字符串

### 输出

- **用户名** ：将获取到的用户名保存到此变量。仅支持字符串变量和字符串
- **密码** ：将获取到的密码保存到此变量。仅支持字符串变量和字符串

## 操作样例

1. 拖入 **获取 Windows 凭据** 组件到设计面板，设置凭据名 "test01"，设置变量“pwd”，“userName”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-1.png)

2. 在电脑凭据管理器里新建一个普通凭据，凭据名：“test01”，用户名：“shirley”，密码：“123456”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-2.png)

3. 拖入 **写入日志** 组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-3.png)

4. 运行流程，控制台输出根据凭据名查找的用户名和密码：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getWindows-4.png)
